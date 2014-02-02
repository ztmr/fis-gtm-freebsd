GT.M for FreeBSD/amd64 (native port)

At first, you should have installed ncurses and libexecinfo packages.
You can get them from BSD ports or in binary form as follows:
# pkg_add -r ncurses
# pkg_add -r libexecinfo

The rest is very similar as on all the other GT.M platforms.
See below for an example console listing:

tmr@siubhan:~$ 
tmr@siubhan:~$ uname -rom
FreeBSD 9.0-RELEASE amd64
tmr@siubhan:~$ 
tmr@siubhan:~$ 
tmr@siubhan:~$ cd gtm_V60000_freebsd_x8664
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ setenv gtm_dist `pwd`
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ ./mumps -r GDE
%GDE-I-GDUSEDEFS, Using defaults for Global Directory 
        /usr/home/tmr/gtm_V60000_freebsd_x8664/mumps.gld

GDE> exit
%GDE-I-VERIFY, Verification OK

%GDE-I-GDCREATE, Creating Global Directory file 
        /usr/home/tmr/gtm_V60000_freebsd_x8664/mumps.gld
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ ./mupip create
Created file /usr/home/tmr/gtm_V60000_freebsd_x8664/mumps.dat
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ 
tmr@siubhan:~/gtm_V60000_freebsd_x8664$ ./mumps -di

GTM>w $zrou

GTM>s $zrou="/home/tmr/ $gtm_dist/"

GTM>D ^%GD

Global Directory

Global ^

Total of 0 globals.

GTM>D SHOW^ZTMR

MUMPS version is: GT.M V6.0-000 FreeBSD x86_64

Code of this routine:

ZTMR W "Hello World!",! Q
ModuleID() Q $P($ZPOS,"^",2)
SHOW
  W !,"MUMPS version is: ",$ZV,!!
  W "Code of this routine:",!!
  ZP @("^"_$$ModuleID) W "----",!!,"Let's call us:",!
  X "D ^"_$$ModuleID W !!
  W "Test globals:",!
  K ^zFoo
  F i=0:1:25 S ^zFoo(i)=$C($A("a")+i)
  ZWR ^zFoo
  W !!,"Database allocation stats:",!
  D ^%FREECNT W !
  Q
----

Let's call us:
Hello World!


Test globals:
^zFoo(0)="a"
^zFoo(1)="b"
^zFoo(2)="c"
^zFoo(3)="d"
^zFoo(4)="e"
^zFoo(5)="f"
^zFoo(6)="g"
^zFoo(7)="h"
^zFoo(8)="i"
^zFoo(9)="j"
^zFoo(10)="k"
^zFoo(11)="l"
^zFoo(12)="m"
^zFoo(13)="n"
^zFoo(14)="o"
^zFoo(15)="p"
^zFoo(16)="q"
^zFoo(17)="r"
^zFoo(18)="s"
^zFoo(19)="t"
^zFoo(20)="u"
^zFoo(21)="v"
^zFoo(22)="w"
^zFoo(23)="x"
^zFoo(24)="y"
^zFoo(25)="z"


Database allocation stats:
Region          Free     Total          Database file
------          ----     -----          -------------
DEFAULT           96       100 ( 96.0%) /usr/home/tmr/gtm_V60000_freebsd_x8664/mumps.dat


GTM>h
tmr@siubhan:~/gtm_V60000_freebsd_x8664$
