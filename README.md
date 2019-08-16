# patch-uWSGI
patch Python uWSGI(flask) for legacy platform


# platform

※ 이문서는 Fedora Core 3, CentOS 4 그리고 5를 기준으로 작성된 문서이며, CentOS 6이상의 platform에서는 아래의 오류를
해결하기 귀한 과정이 생략된다.

python uwsgi 2.0.17을 CentOS-5(EL5) 이하에서 build를 하면 되면 2가지 오류를 만나게 된다.

첫째로 아래와 같은 오류메세지를 만나는데,

```
core/event.c:1112:25: sys/inotify.h: No such file or directory
core/event.c: In function `event_queue_add_file_monitor':
core/event.c:1128: warning: implicit declaration of function `inotify_init'
core/event.c:1136: warning: implicit declaration of function
`inotify_add_watch'
core/event.c:1136: error: `IN_ATTRIB' undeclared (first use in this
function)
core/event.c:1136: error: (Each undeclared identifier is reported only once
core/event.c:1136: error: for each function it appears in.)
core/event.c:1136: error: `IN_CREATE' undeclared (first use in this
function)
core/event.c:1136: error: `IN_DELETE' undeclared (first use in this
function)
core/event.c:1136: error: `IN_DELETE_SELF' undeclared (first use in this
function)
core/event.c:1136: error: `IN_MODIFY' undeclared (first use in this
function)
core/event.c:1136: error: `IN_MOVE_SELF' undeclared (first use in this
function)
core/event.c:1136: error: `IN_MOVED_FROM' undeclared (first use in this
function)
core/event.c:1136: error: `IN_MOVED_TO' undeclared (first use in this
function)
core/event.c: In function `event_queue_ack_file_monitor':
core/event.c:1153: error: storage size of 'ie' isn't known
core/event.c:1157: error: invalid application of `sizeof' to incomplete
type `inotify_event'
core/event.c:1165: error: invalid application of `sizeof' to incomplete
type `inotify_event'
core/event.c:1170: error: invalid application of `sizeof' to incomplete
type `inotify_event'
core/event.c:1178: error: invalid application of `sizeof' to incomplete
type `inotify_event'
core/event.c:1178: warning: division by zero
core/event.c:1183: error: invalid use of undefined type `struct
inotify_event'
core/event.c:1183: error: dereferencing pointer to incomplete type
core/event.c:1186: error: dereferencing pointer to incomplete type
core/event.c:1153: warning: unused variable `ie'
```

이는 파일 시스템 이벤트 통보 기능을 제공해 주는 리눅스 커널 서브시스템중 하나인데 inotify 함수를 찾지 못 해 발생하는 오류로 설치를 통해
에러를 해결 할 수 있다.

설치에 진행된 플랫폼이 CentOS-4 이었기에 아래 link에서 rpm을 다운받아 설치하면 된다.

ᄆ i
https://rpmfind.net/linux/dag/redhat/el4/en/i386/dag/RPMS/inotify-tools-3.13-1.el4.rf.i386.rpm
https://rpmfind.net/linux/dag/redhat/el4/en/i386/dag/RPMS/inotify-tools-3.13-devel-1.el4.rf.i386.rpm

ᄆ x
https://rpmfind.net/linux/dag/redhat/el4/en/i386/dag/RPMS/inotify-tools-3.13-1.el4.rf.i686.rpm
https://rpmfind.net/linux/dag/redhat/el4/en/x86_64/dag/RPMS/inotify-tools-devel-3.13-1.el4.rf.x86_64.rpm

rpm 설치후에는 header 파일들을 link를 걸어준다.
ln -sf /usr/include/inotifytools/*.h /usr/include/sys/

두번째로, 첫번째 이슈를 해결후 다시 build를 진행하면 아래와 같은 오류가 추가로 발생하게 되는데,

```
core/utils.o(.text+0x67c3): In function `uwsgi_as_root':
: undefined reference to `unshare'
core/utils.o(.text+0x68e3): In function `uwsgi_as_root':
: undefined reference to `unshare'
collect2: ld returned 1 exit status
*** error linking uWSGI ***
```
uWSGI document에서 찾아본 결과 CentOS 5 이하의 오래된 시스템에서 발생할 수 있는 오류이다.

참조링크 : [http://uwsgi-docs.readthedocs.io/en/latest/ThingsToKnow.html](http://uwsgi-docs.readthedocs.io/en/latest/ThingsToKnow.html)
[http://uwsgi-docs.readthedocs.io/en/latest/Namespaces.html](http://uwsgi-docs.readthedocs.io/en/latest/Namespaces.html)

# 참조링크 중 발췌
Some Linux distributions (read: Debian 4 Etch, RHEL / CentOS 5) make a mix of newer kernels with very old userspace.
This kind of combination can make the uWSGI build system spit out errors (most notably on unshare(), pthread locking,
inotify...). You can force uWSGI to configure itself for an older system prefixing the ‘make’ (or whatever way you use
to build it) with CFLAGS="-DOBSOLETE_LINUX_KERNEL"

위 발췌한 문서에 따르면 몇몇의 리눅스 배포판에서 오래된 사용자 공간을 새로운 커널과 혼합하여 만들어 졌으며 이런 종류의 조합은 uWSGI
빌드 시스템에서 오류를 발생할 수 있다는 것이다.
make를 하기이전에 CFLAGS 값을 지정하여 빌드를 하면 해결된다고 문서에는 적혀 있으나 테스트 결과 동일하게 오류가 발생하였으며, 오류가
발생하는 것은 아래 링크의
기능으로 인하여 발생하는 부분인데 확인결과 우리 시스템에서는 적용하지 않는 부분으로 이슈가 발생하는 source를 patch하여 설치를 완료 할
수 있었다.
[http://uwsgi-docs.readthedocs.io/en/latest/Namespaces.html](http://uwsgi-docs.readthedocs.io/en/latest/Namespaces.html)

```
[root@xxx_que0004 sdev_src]# cat uwsgi_2.0.17_util.c.patch
--- core/utils.c 2018-02-27 03:34:40.000000000 +
+++ core/utils.c.patch 2018-06-12 15:08:34.000000000 +
@@ -338,29 +338,6 @@
```
```
int in_jail = 0;

-#if defined(__linux__) && !defined(OBSOLETE_LINUX_KERNEL)

- if (uwsgi.unshare && !uwsgi.reloads) {
-
- if (unshare(uwsgi.unshare)) {
- uwsgi_error("unshare()");
- exit(1);
- }

- else {
- uwsgi_log("[linux-namespace] applied unshare()
mask: %d\n", uwsgi.unshare);
- }
-
-#ifdef CLONE_NEWUSER
- if (uwsgi.unshare & CLONE_NEWUSER) {
- if (setuid(0)) {
- uwsgi_error("uwsgi_as_root()/setuid(0)");
- exit(1);
- }
- }
-#endif
- in_jail = 1;
- }
-#endif
-
#ifdef UWSGI_CAP
if (uwsgi.cap && uwsgi.cap_count > 0 && !uwsgi.reloads) {
uwsgi_apply_cap(uwsgi.cap, uwsgi.cap_count);
@@ -637,27 +614,6 @@
}
#endif

-#if defined(__linux__) && !defined(OBSOLETE_LINUX_KERNEL)

- if (uwsgi.unshare2 && !uwsgi.reloads) {
-
- if (unshare(uwsgi.unshare2)) {
- uwsgi_error("unshare()");
- exit(1);
- }
- else {
- uwsgi_log("[linux-namespace] applied unshare()
mask: %d\n", uwsgi.unshare2);
- }
-#ifdef CLONE_NEWUSER
- if (uwsgi.unshare2 & CLONE_NEWUSER) {
- if (setuid(0)) {
- uwsgi_error("uwsgi_as_root()/setuid(0)");
- exit(1);
- }
- }
-#endif
- in_jail = 1;
- }
-#endif


if (uwsgi.refork_as_root) {
uwsgi_log("re-fork()ing...\n");
```

