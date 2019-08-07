# patch-uWSGI
patch uWSGI(flask) for legacy platform

Message-ID: \&lt;785725533.1.1565215098902.JavaMail.root@wiki.simplexi.com\&gt;

Subject: Exported From Confluence

MIME-Version: 1.0

Content-Type: multipart/related;

 boundary=&quot;----=\_Part\_0\_1015394655.1565215098888&quot;

------=\_Part\_0\_1015394655.1565215098888

Content-Type: text/html; charset=UTF-8

Content-Transfer-Encoding: quoted-printable

Content-Location: file:///C:/exported.html

\&lt;html xmlns:o=3D&#39;urn:schemas-microsoft-com:office:office&#39;

      xmlns:w=3D&#39;urn:schemas-microsoft-com:office:word&#39;

      xmlns:v=3D&#39;urn:schemas-microsoft-com:vml&#39;

      xmlns=3D&#39;urn:w3-org-ns:HTML&#39;\&gt;

\&lt;head\&gt;

    \&lt;meta http-equiv=3D&quot;Content-Type&quot; content=3D&quot;text/html; charset=3Dutf-8=

&quot;\&gt;

    \&lt;title\&gt;[=EC=99=84=EB=A3=8C][=EC=9D=B4=EC=9E=A5=EC=9E=AC] EC=EC=86=94=EB=

=A3=A8=EC=85=98 python uWSGI(flask) build for legacy platform\&lt;/title\&gt;

    \&lt;!--[if gte mso 9]\&gt;

    \&lt;xml\&gt;

        \&lt;o:OfficeDocumentSettings\&gt;

            \&lt;o:TargetScreenSize\&gt;1024x640\&lt;/o:TargetScreenSize\&gt;

            \&lt;o:PixelsPerInch\&gt;72\&lt;/o:PixelsPerInch\&gt;

            \&lt;o:AllowPNG/\&gt;

        \&lt;/o:OfficeDocumentSettings\&gt;

        \&lt;w:WordDocument\&gt;

            \&lt;w:View\&gt;Print\&lt;/w:View\&gt;

            \&lt;w:Zoom\&gt;90\&lt;/w:Zoom\&gt;

            \&lt;w:DoNotOptimizeForBrowser/\&gt;

        \&lt;/w:WordDocument\&gt;

    \&lt;/xml\&gt;

    \&lt;![endif]--\&gt;

    \&lt;style\&gt;

                \&lt;!--

        @page Section1 {

            size: 8.5in 11.0in;

            margin: 1.0in;

            mso-header-margin: .5in;

            mso-footer-margin: .5in;

            mso-paper-source: 0;

        }

        table {

            border: solid 1px;

            border-collapse: collapse;

        }

        table td, table th {

            border: solid 1px;

            padding: 5px;

        }

        td {

            page-break-inside: avoid;

        }

        tr {

            page-break-after: avoid;

        }

        div.Section1 {

            page: Section1;

        }

        /\* Confluence print stylesheet. Common to all themes for print medi=

a \*/

/\* Full of !important until we improve batching for print CSS \*/

@media print {

    #main {

        padding-bottom: 1em !important; /\* The default padding of 6em is to=

o much for printouts \*/

    }

    body {

        font-family: Arial, Helvetica, FreeSans, sans-serif;

        font-size: 10pt;

        line-height: 1.2;

    }

    body, #full-height-container, #main, #page, #content, .has-personal-sid=

ebar #content {

        background: #fff !important;

        color: #000 !important;

        border: 0 !important;

        width: 100% !important;

        height: auto !important;

        min-height: auto !important;

        margin: 0 !important;

        padding: 0 !important;

        display: block !important;

    }

    a, a:link, a:visited, a:focus, a:hover, a:active {

        color: #000;

    }

    #content h1,

    #content h2,

    #content h3,

    #content h4,

    #content h5,

    #content h6 {

        font-family: Arial, Helvetica, FreeSans, sans-serif;

        page-break-after: avoid;

    }

    pre {

        font-family: Monaco, &quot;Courier New&quot;, monospace;

    }

    #header,

    .aui-header-inner,

    #navigation,

    #sidebar,

    .sidebar,

    #personal-info-sidebar,

    .ia-fixed-sidebar,

    .page-actions,

    .navmenu,

    .ajs-menu-bar,

    .noprint,

    .inline-control-link,

    .inline-control-link a,

    a.show-labels-editor,

    .global-comment-actions,

    .comment-actions,

    .quick-comment-container,

    #addcomment {

        display: none !important;

    }

    /\* CONF-28544 cannot print multiple pages in IE \*/

    #splitter-content {

        position: relative !important;

    }

    .comment .date::before {

        content: none !important; /\* remove middot for print view \*/

    }

    h1.pagetitle img {

        height: auto;

        width: auto;

    }

    .print-only {

        display: block;

    }

    #footer {

        position: relative !important; /\* CONF-17506 Place the footer at en=

d of the content \*/

        margin: 0;

        padding: 0;

        background: none;

        clear: both;

    }

    #poweredby {

        border-top: none;

        background: none;

    }

    #poweredby li.print-only {

        display: list-item;

        font-style: italic;

    }

    #poweredby li.noprint {

        display: none;

    }

    /\* no width controls in print \*/

    .wiki-content .table-wrap,

    .wiki-content p,

    .panel .codeContent,

    .panel .codeContent pre,

    .image-wrap {

        overflow: visible !important;

    }

    /\* TODO - should this work? \*/

    #children-section,

    #comments-section .comment,

    #comments-section .comment .comment-body,

    #comments-section .comment .comment-content,

    #comments-section .comment p {

        page-break-inside: avoid;

    }

    #page-children a {

        text-decoration: none;

    }

    /\*\*

     hide twixies

     the specificity here is a hack because print styles

     are getting loaded before the base styles. \*/

    #comments-section.pageSection .section-header,

    #comments-section.pageSection .section-title,

    #children-section.pageSection .section-header,

    #children-section.pageSection .section-title,

    .children-show-hide {

        padding-left: 0;

        margin-left: 0;

    }

    .children-show-hide.icon {

        display: none;

    }

    /\* personal sidebar \*/

    .has-personal-sidebar #content {

        margin-right: 0px;

    }

    .has-personal-sidebar #content .pageSection {

        margin-right: 0px;

    }

    .no-print, .no-print \* {

        display: none !important;

    }

}

--\&gt;

    \&lt;/style\&gt;

\&lt;/head\&gt;

\&lt;body\&gt;

    \&lt;h1\&gt;[=EC=99=84=EB=A3=8C][=EC=9D=B4=EC=9E=A5=EC=9E=AC] EC=EC=86=94=EB=A3=

=A8=EC=85=98 python uWSGI(flask) build for legacy platform\&lt;/h1\&gt;

    \&lt;div class=3D&quot;Section1&quot;\&gt;

        \&lt;p\&gt;\&lt;br\&gt;\&lt;/p\&gt;

\&lt;p\&gt;\&lt;strong\&gt;=E2=80=BB =EC=9D=B4=EB=AC=B8=EC=84=9C=EB=8A=94 EC=EC=86=94=EB=A3=

=A8=EC=85=98=EC=9D=98 Fedora Core 3, CentOS 4 =EA=B7=B8=EB=A6=AC=EA=B3=A0 5=

=EB=A5=BC =EA=B8=B0=EC=A4=80=EC=9C=BC=EB=A1=9C =EC=9E=91=EC=84=B1=EB=90=9C =

=EB=AC=B8=EC=84=9C=EC=9D=B4=EB=A9=B0, CentOS 6=EC=9D=B4=EC=83=81=EC=9D=98 p=

latform=EC=97=90=EC=84=9C=EB=8A=94 =EC=95=84=EB=9E=98=EC=9D=98 =EC=98=A4=EB=

=A5=98=EB=A5=BC =ED=95=B4=EA=B2=B0=ED=95=98=EA=B8=B0 =EA=B7=80=ED=95=9C =EA=

=B3=BC=EC=A0=95=EC=9D=B4 =EC=83=9D=EB=9E=B5=EB=90=9C=EB=8B=A4.\&lt;/strong\&gt;\&lt;/p\&gt;

\&lt;p\&gt;python uwsgi 2.0.17=EC=9D=84 CentOS-5(EL5) =EC=9D=B4=ED=95=98=EC=97=90=

=EC=84=9C build=EB=A5=BC =ED=95=98=EB=A9=B4 =EB=90=98=EB=A9=B4 2=EA=B0=80=

=EC=A7=80 =EC=98=A4=EB=A5=98=EB=A5=BC =EB=A7=8C=EB=82=98=EA=B2=8C =EB=90=9C=

=EB=8B=A4.\&lt;/p\&gt;

\&lt;p\&gt;=EC=B2=AB=EC=A7=B8=EB=A1=9C =EC=95=84=EB=9E=98=EC=99=80 =EA=B0=99=EC=9D=

=80 =EC=98=A4=EB=A5=98=EB=A9=94=EC=84=B8=EC=A7=80=EB=A5=BC =EB=A7=8C=EB=82=

=98=EB=8A=94=EB=8D=B0,\&lt;/p\&gt;

\&lt;div class=3D&quot;code panel pdl&quot; style=3D&quot;border-width: 1px;&quot;\&gt;

\&lt;div class=3D&quot;codeContent panelContent pdl&quot;\&gt;=20

\&lt;pre class=3D&quot;syntaxhighlighter-pre&quot; data-syntaxhighlighter-params=3D&quot;brush=

: bash; gutter: false; theme: Emacs&quot; data-theme=3D&quot;Emacs&quot;\&gt;core/event.c:1112=

:25: sys/inotify.h: No such file or directory

core/event.c: In function `event\_queue\_add\_file\_monitor&#39;:

core/event.c:1128: warning: implicit declaration of function `inotify\_init&#39;

core/event.c:1136: warning: implicit declaration of function `inotify\_add\_w=

atch&#39;

core/event.c:1136: error: `IN\_ATTRIB&#39; undeclared (first use in this functio=

n)

core/event.c:1136: error: (Each undeclared identifier is reported only once

core/event.c:1136: error: for each function it appears in.)

core/event.c:1136: error: `IN\_CREATE&#39; undeclared (first use in this functio=

n)

core/event.c:1136: error: `IN\_DELETE&#39; undeclared (first use in this functio=

n)

core/event.c:1136: error: `IN\_DELETE\_SELF&#39; undeclared (first use in this fu=

nction)

core/event.c:1136: error: `IN\_MODIFY&#39; undeclared (first use in this functio=

n)

core/event.c:1136: error: `IN\_MOVE\_SELF&#39; undeclared (first use in this func=

tion)

core/event.c:1136: error: `IN\_MOVED\_FROM&#39; undeclared (first use in this fun=

ction)

core/event.c:1136: error: `IN\_MOVED\_TO&#39; undeclared (first use in this funct=

ion)

core/event.c: In function `event\_queue\_ack\_file\_monitor&#39;:

core/event.c:1153: error: storage size of &#39;ie&#39; isn&#39;t known

core/event.c:1157: error: invalid application of `sizeof&#39; to incomplete typ=

e `inotify\_event&#39;

core/event.c:1165: error: invalid application of `sizeof&#39; to incomplete typ=

e `inotify\_event&#39;

core/event.c:1170: error: invalid application of `sizeof&#39; to incomplete typ=

e `inotify\_event&#39;

core/event.c:1178: error: invalid application of `sizeof&#39; to incomplete typ=

e `inotify\_event&#39;

core/event.c:1178: warning: division by zero

core/event.c:1183: error: invalid use of undefined type `struct inotify\_eve=

nt&#39;

core/event.c:1183: error: dereferencing pointer to incomplete type

core/event.c:1186: error: dereferencing pointer to incomplete type

core/event.c:1153: warning: unused variable `ie&#39;\&lt;/pre\&gt;=20

\&lt;/div\&gt;

\&lt;/div\&gt;

\&lt;p\&gt;\&lt;br\&gt;\&lt;/p\&gt;

\&lt;p\&gt;=EC=9D=B4=EB=8A=94 =ED=8C=8C=EC=9D=BC =EC=8B=9C=EC=8A=A4=ED=85=9C =EC=9D=

=B4=EB=B2=A4=ED=8A=B8 =ED=86=B5=EB=B3=B4 =EA=B8=B0=EB=8A=A5=EC=9D=84 =EC=A0=

=9C=EA=B3=B5=ED=95=B4 =EC=A3=BC=EB=8A=94 =EB=A6=AC=EB=88=85=EC=8A=A4 =EC=BB=

=A4=EB=84=90 =EC=84=9C=EB=B8=8C=EC=8B=9C=EC=8A=A4=ED=85=9C=EC=A4=91 =ED=95=

=98=EB=82=98=EC=9D=B8=EB=8D=B0 inotify =ED=95=A8=EC=88=98=EB=A5=BC =EC=B0=

=BE=EC=A7=80 =EB=AA=BB =ED=95=B4 =EB=B0=9C=EC=83=9D=ED=95=98=EB=8A=94 =EC=

=98=A4=EB=A5=98=EB=A1=9C =EC=84=A4=EC=B9=98=EB=A5=BC =ED=86=B5=ED=95=B4\&lt;br\&gt;=

=EC=97=90=EB=9F=AC=EB=A5=BC =ED=95=B4=EA=B2=B0 =ED=95=A0 =EC=88=98 =EC=9E=

=88=EB=8B=A4.\&lt;/p\&gt;

\&lt;p\&gt;=EC=84=A4=EC=B9=98=EC=97=90 =EC=A7=84=ED=96=89=EB=90=9C =ED=94=8C=EB=9E=

=AB=ED=8F=BC=EC=9D=B4 CentOS-4 =EC=9D=B4=EC=97=88=EA=B8=B0=EC=97=90 =EC=95=

=84=EB=9E=98 link=EC=97=90=EC=84=9C rpm=EC=9D=84 =EB=8B=A4=EC=9A=B4=EB=B0=

=9B=EC=95=84 =EC=84=A4=EC=B9=98=ED=95=98=EB=A9=B4 =EB=90=9C=EB=8B=A4.\&lt;/p\&gt;

\&lt;p\&gt;=E3=85=81 i386\&lt;br\&gt;\&lt;a href=3D&quot;https://rpmfind.net/linux/dag/redhat/el4/en=

/i386/dag/RPMS/inotify-tools-3.13-1.el4.rf.i386.rpm&quot; class=3D&quot;external-link=

&quot; rel=3D&quot;nofollow&quot;\&gt;https://rpmfind.net/linux/dag/redhat/el4/en/i386/dag/RPM=

S/inotify-tools-3.13-1.el4.rf.i386.rpm\&lt;/a\&gt;\&lt;br\&gt;\&lt;a href=3D&quot;https://rpmfind.ne=

t/linux/dag/redhat/el4/en/i386/dag/RPMS/inotify-tools-3.13-devel-1.el4.rf.i=

386.rpm&quot; class=3D&quot;external-link&quot; rel=3D&quot;nofollow&quot;\&gt;https://rpmfind.net/linux=

/dag/redhat/el4/en/i386/dag/RPMS/inotify-tools-3.13-devel-1.el4.rf.i386.rpm=

\&lt;/a\&gt;\&lt;/p\&gt;

\&lt;p\&gt;=E3=85=81 x64\&lt;br\&gt;\&lt;a href=3D&quot;https://rpmfind.net/linux/dag/redhat/el4/en/=

i386/dag/RPMS/inotify-tools-3.13-1.el4.rf.i686.rpm&quot; class=3D&quot;external-link&quot;=

 rel=3D&quot;nofollow&quot;\&gt;https://rpmfind.net/linux/dag/redhat/el4/en/i386/dag/RPMS=

/inotify-tools-3.13-1.el4.rf.i686.rpm\&lt;/a\&gt;\&lt;br\&gt;\&lt;a href=3D&quot;https://rpmfind.net=

/linux/dag/redhat/el4/en/x86\_64/dag/RPMS/inotify-tools-devel-3.13-1.el4.rf.=

x86\_64.rpm&quot; class=3D&quot;external-link&quot; rel=3D&quot;nofollow&quot;\&gt;https://rpmfind.net/li=

nux/dag/redhat/el4/en/x86\_64/dag/RPMS/inotify-tools-devel-3.13-1.el4.rf.x86=

\_64.rpm\&lt;/a\&gt;\&lt;/p\&gt;

\&lt;p\&gt;rpm =EC=84=A4=EC=B9=98=ED=9B=84=EC=97=90=EB=8A=94 header =ED=8C=8C=EC=9D=

=BC=EB=93=A4=EC=9D=84 link=EB=A5=BC =EA=B1=B8=EC=96=B4=EC=A4=80=EB=8B=A4.\&lt;b=

r\&gt;ln -sf /usr/include/inotifytools/\*.h /usr/include/sys/\&lt;/p\&gt;

\&lt;p\&gt;\&lt;br\&gt;=EB=91=90=EB=B2=88=EC=A7=B8=EB=A1=9C, =EC=B2=AB=EB=B2=88=EC=A7=B8 =

=EC=9D=B4=EC=8A=88=EB=A5=BC =ED=95=B4=EA=B2=B0=ED=9B=84 =EB=8B=A4=EC=8B=9C =

build=EB=A5=BC =EC=A7=84=ED=96=89=ED=95=98=EB=A9=B4 =EC=95=84=EB=9E=98=EC=

=99=80 =EA=B0=99=EC=9D=80 =EC=98=A4=EB=A5=98=EA=B0=80 =EC=B6=94=EA=B0=80=EB=

=A1=9C =EB=B0=9C=EC=83=9D=ED=95=98=EA=B2=8C =EB=90=98=EB=8A=94=EB=8D=B0,\&lt;/p=

\&gt;

\&lt;div class=3D&quot;code panel pdl&quot; style=3D&quot;border-width: 1px;&quot;\&gt;

\&lt;div class=3D&quot;codeContent panelContent pdl&quot;\&gt;=20

\&lt;pre class=3D&quot;syntaxhighlighter-pre&quot; data-syntaxhighlighter-params=3D&quot;brush=

: bash; gutter: false; theme: Emacs&quot; data-theme=3D&quot;Emacs&quot;\&gt;core/utils.o(.tex=

t+0x67c3): In function `uwsgi\_as\_root&#39;:

: undefined reference to `unshare&#39;

core/utils.o(.text+0x68e3): In function `uwsgi\_as\_root&#39;:

: undefined reference to `unshare&#39;

collect2: ld returned 1 exit status

\*\*\* error linking uWSGI \*\*\*\&lt;/pre\&gt;=20

\&lt;/div\&gt;

\&lt;/div\&gt;

\&lt;p\&gt;\&lt;br\&gt;\&lt;/p\&gt;

\&lt;p\&gt;uWSGI document=EC=97=90=EC=84=9C =EC=B0=BE=EC=95=84=EB=B3=B8 =EA=B2=B0=

=EA=B3=BC CentOS 5 =EC=9D=B4=ED=95=98=EC=9D=98 =EC=98=A4=EB=9E=98=EB=90=9C =

=EC=8B=9C=EC=8A=A4=ED=85=9C=EC=97=90=EC=84=9C =EB=B0=9C=EC=83=9D=ED=95=A0 =

=EC=88=98 =EC=9E=88=EB=8A=94 =EC=98=A4=EB=A5=98=EC=9D=B4=EB=8B=A4.\&lt;/p\&gt;

\&lt;p\&gt;=EC=B0=B8=EC=A1=B0=EB=A7=81=ED=81=AC : \&lt;a href=3D&quot;http://uwsgi-docs.read=

thedocs.io/en/latest/ThingsToKnow.html&quot; class=3D&quot;external-link&quot; rel=3D&quot;nofo=

llow&quot;\&gt;http://uwsgi-docs.readthedocs.io/en/latest/ThingsToKnow.html\&lt;/a\&gt; \&lt;br\&gt;=

 \&lt;a href=3D&quot;http://uwsgi-docs.readthedocs.io/en/latest/Namespaces.html&quot; cla=

ss=3D&quot;external-link&quot; rel=3D&quot;nofollow&quot;\&gt;http://uwsgi-docs.readthedocs.io/en/l=

atest/Namespaces.html\&lt;/a\&gt;\&lt;br\&gt; \&lt;br\&gt;# =EC=B0=B8=EC=A1=B0=EB=A7=81=ED=81=AC =

=EC=A4=91 =EB=B0=9C=EC=B7=8C\&lt;br\&gt;Some Linux distributions (read: Debian 4 Et=

ch, RHEL / CentOS 5) make a mix of newer kernels with very old userspace.\&lt;b=

r\&gt;This kind of combination can make the uWSGI build system spit out errors =

(most notably on unshare(), pthread locking,\&lt;br\&gt;inotify=E2=80=A6). You can =

force uWSGI to configure itself for an older system prefixing the =E2=80=98=

make=E2=80=99 (or whatever way you use\&lt;br\&gt; to build it) with CFLAGS=3D&quot;-DOB=

SOLETE\_LINUX\_KERNEL&quot;\&lt;br\&gt; \&lt;br\&gt;=EC=9C=84 =EB=B0=9C=EC=B7=8C=ED=95=9C =EB=AC=

=B8=EC=84=9C=EC=97=90 =EB=94=B0=EB=A5=B4=EB=A9=B4 =EB=AA=87=EB=AA=87=EC=9D=

=98 =EB=A6=AC=EB=88=85=EC=8A=A4 =EB=B0=B0=ED=8F=AC=ED=8C=90=EC=97=90=EC=84=

=9C =EC=98=A4=EB=9E=98=EB=90=9C =EC=82=AC=EC=9A=A9=EC=9E=90 =EA=B3=B5=EA=B0=

=84=EC=9D=84 =EC=83=88=EB=A1=9C=EC=9A=B4 =EC=BB=A4=EB=84=90=EA=B3=BC =ED=98=

=BC=ED=95=A9=ED=95=98=EC=97=AC =EB=A7=8C=EB=93=A4=EC=96=B4 =EC=A1=8C=EC=9C=

=BC=EB=A9=B0 =EC=9D=B4=EB=9F=B0 =EC=A2=85=EB=A5=98=EC=9D=98 =EC=A1=B0=ED=95=

=A9=EC=9D=80 uWSGI =EB=B9=8C=EB=93=9C =EC=8B=9C=EC=8A=A4=ED=85=9C=EC=97=90=

=EC=84=9C =EC=98=A4=EB=A5=98=EB=A5=BC =EB=B0=9C=EC=83=9D=ED=95=A0 =EC=88=98=

 =EC=9E=88=EB=8B=A4=EB=8A=94 =EA=B2=83=EC=9D=B4=EB=8B=A4.\&lt;br\&gt;make=EB=A5=BC =

=ED=95=98=EA=B8=B0=EC=9D=B4=EC=A0=84=EC=97=90 CFLAGS =EA=B0=92=EC=9D=84 =EC=

=A7=80=EC=A0=95=ED=95=98=EC=97=AC =EB=B9=8C=EB=93=9C=EB=A5=BC =ED=95=98=EB=

=A9=B4 =ED=95=B4=EA=B2=B0=EB=90=9C=EB=8B=A4=EA=B3=A0 =EB=AC=B8=EC=84=9C=EC=

=97=90=EB=8A=94 =EC=A0=81=ED=98=80 =EC=9E=88=EC=9C=BC=EB=82=98 =ED=85=8C=EC=

=8A=A4=ED=8A=B8 =EA=B2=B0=EA=B3=BC =EB=8F=99=EC=9D=BC=ED=95=98=EA=B2=8C =EC=

=98=A4=EB=A5=98=EA=B0=80 =EB=B0=9C=EC=83=9D=ED=95=98=EC=98=80=EC=9C=BC=EB=

=A9=B0, =EC=98=A4=EB=A5=98=EA=B0=80 =EB=B0=9C=EC=83=9D=ED=95=98=EB=8A=94 =

=EA=B2=83=EC=9D=80 =EC=95=84=EB=9E=98 =EB=A7=81=ED=81=AC=EC=9D=98\&lt;br\&gt;=EA=B8=

=B0=EB=8A=A5=EC=9C=BC=EB=A1=9C =EC=9D=B8=ED=95=98=EC=97=AC =EB=B0=9C=EC=83=

=9D=ED=95=98=EB=8A=94 =EB=B6=80=EB=B6=84=EC=9D=B8=EB=8D=B0 =ED=99=95=EC=9D=

=B8=EA=B2=B0=EA=B3=BC =EC=9A=B0=EB=A6=AC =EC=8B=9C=EC=8A=A4=ED=85=9C=EC=97=

=90=EC=84=9C=EB=8A=94 =EC=A0=81=EC=9A=A9=ED=95=98=EC=A7=80 =EC=95=8A=EB=8A=

=94 =EB=B6=80=EB=B6=84=EC=9C=BC=EB=A1=9C =EC=9D=B4=EC=8A=88=EA=B0=80 =EB=B0=

=9C=EC=83=9D=ED=95=98=EB=8A=94 source=EB=A5=BC patch=ED=95=98=EC=97=AC =EC=

=84=A4=EC=B9=98=EB=A5=BC =EC=99=84=EB=A3=8C =ED=95=A0 =EC=88=98 =EC=9E=88=

=EC=97=88=EB=8B=A4.\&lt;br\&gt;\&lt;a href=3D&quot;http://uwsgi-docs.readthedocs.io/en/lates=

t/Namespaces.html&quot; class=3D&quot;external-link&quot; rel=3D&quot;nofollow&quot;\&gt;http://uwsgi-do=

cs.readthedocs.io/en/latest/Namespaces.html\&lt;/a\&gt;\&lt;/p\&gt;

\&lt;p\&gt;\&lt;br\&gt;\&lt;/p\&gt;

\&lt;div class=3D&quot;code panel pdl&quot; style=3D&quot;border-width: 1px;&quot;\&gt;

\&lt;div class=3D&quot;codeContent panelContent pdl&quot;\&gt;=20

\&lt;pre class=3D&quot;syntaxhighlighter-pre&quot; data-syntaxhighlighter-params=3D&quot;brush=

: bash; gutter: false; theme: Emacs&quot; data-theme=3D&quot;Emacs&quot;\&gt;[root@xxx\_que0004=

 sdev\_src]# cat uwsgi\_2.0.17\_util.c.patch=20

--- core/utils.c        2018-02-27 03:34:40.000000000 +0900

+++ core/utils.c.patch  2018-06-12 15:08:34.000000000 +0900

@@ -338,29 +338,6 @@

=20

        int in\_jail =3D 0;

=20

-#if defined(\_\_linux\_\_) &amp;amp;&amp;amp; !defined(OBSOLETE\_LINUX\_KERNEL)

-       if (uwsgi.unshare &amp;amp;&amp;amp; !uwsgi.reloads) {

-

-               if (unshare(uwsgi.unshare)) {

-                       uwsgi\_error(&quot;unshare()&quot;);

-                       exit(1);

-               }

-               else {

-                       uwsgi\_log(&quot;[linux-namespace] applied unshare() mask=

: %d\n&quot;, uwsgi.unshare);

-               }

-

-#ifdef CLONE\_NEWUSER

-               if (uwsgi.unshare &amp;amp; CLONE\_NEWUSER) {

-                       if (setuid(0)) {

-                               uwsgi\_error(&quot;uwsgi\_as\_root()/setuid(0)&quot;);

-                               exit(1);

-                       }

-               }

-#endif

-               in\_jail =3D 1;

-       }

-#endif

-

 #ifdef UWSGI\_CAP

        if (uwsgi.cap &amp;amp;&amp;amp; uwsgi.cap\_count &amp;gt; 0 &amp;amp;&amp;amp; !uwsgi.r=

eloads) {

                uwsgi\_apply\_cap(uwsgi.cap, uwsgi.cap\_count);

@@ -637,27 +614,6 @@

        }

 #endif

=20

-#if defined(\_\_linux\_\_) &amp;amp;&amp;amp; !defined(OBSOLETE\_LINUX\_KERNEL)

-       if (uwsgi.unshare2 &amp;amp;&amp;amp; !uwsgi.reloads) {

-

-               if (unshare(uwsgi.unshare2)) {

-                       uwsgi\_error(&quot;unshare()&quot;);

-                       exit(1);

-               }

-               else {

-                       uwsgi\_log(&quot;[linux-namespace] applied unshare() mask=

: %d\n&quot;, uwsgi.unshare2);

-               }

-#ifdef CLONE\_NEWUSER

-               if (uwsgi.unshare2 &amp;amp; CLONE\_NEWUSER) {

-                       if (setuid(0)) {

-                               uwsgi\_error(&quot;uwsgi\_as\_root()/setuid(0)&quot;);

-                               exit(1);

-                       }

-               }

-#endif

-               in\_jail =3D 1;

-       }

-#endif

=20

        if (uwsgi.refork\_as\_root) {

                uwsgi\_log(&quot;re-fork()ing...\n&quot;);

=09=09=09=09\&lt;/pre\&gt;=20

\&lt;/div\&gt;

\&lt;/div\&gt;

    \&lt;/div\&gt;

\&lt;/body\&gt;

\&lt;/html\&gt;

------=\_Part\_0\_1015394655.1565215098888--
