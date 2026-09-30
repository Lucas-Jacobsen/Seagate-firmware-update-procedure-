Seagate-firmware-update-procedure-

sudo apt update && sudo apt install -y build-essential linux-headers-$(uname -r) virtualbox-guest-utils

9.24

cg@cg-C1001140:~$ sudo mv ~/Documents/lib_20260924/lib/libgssapi.so.3 /usr/lib/x86_64-linux-gnu/
cg@cg-C1001140:~$ sudo mv ~/Documents/lib_20260924/lib/liblber-2.4.so.2 /usr/lib/x86_64-linux-gnu/
cg@cg-C1001140:~$ sudo mv ~/Documents/lib_20260924/lib/libldap_r-2.4.so.2 /usr/lib/x86_64-linux-gnu/

cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$ ls -al 
total 57908
drwxrwxrwx 2 cg cg     4096 Sep 17 08:37  .
drwxrwxr-x 4 cg cg     4096 Sep 17 08:21  ..
-rwxrwxrwx 1 cg cg 10202224 Mar 25  2026  'PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux_64bit'
-rw-rw-rw- 1 cg cg 49049224 Mar 25  2026  libMPFlow.so.1.0.0
-rw-rw-r-- 1 cg cg     8577 Sep 17 08:36  seagate_crash_log.txt
-rw-rw-r-- 1 cg cg    16488 Sep 17 08:37  seagate_journal_log.txt
-rw-rw-r-- 1 cg cg      150 Sep 17 08:33  seagate_upgrade.log

cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$  ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit AUTO
Segmentation fault         (core dumped) ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit AUTO

cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$ sudo ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit AUTO
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
Segmentation fault         (core dumped) sudo ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit AUTO

cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$  ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit 
"Try to close the MPTool, waiting for all thread close..." 

cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$ ldd libMPFlow.so.1.0.0 
	linux-vdso.so.1 (0x000071b73c99a000)
	libldap_r-2.4.so.2 => not found
	libQt5Gui.so.5 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libQt5Gui.so.5 (0x000071b738c00000)
	libQt5Core.so.5 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libQt5Core.so.5 (0x000071b738400000)
	libpthread.so.0 => /usr/lib/x86_64-linux-gnu/libpthread.so.0 (0x000071b73c97c000)
	libstdc++.so.6 => /usr/lib/x86_64-linux-gnu/libstdc++.so.6 (0x000071b738000000)
	libm.so.6 => /usr/lib/x86_64-linux-gnu/libm.so.6 (0x000071b7382da000)
	libgcc_s.so.1 => /usr/lib/x86_64-linux-gnu/libgcc_s.so.1 (0x000071b73c94c000)
	libc.so.6 => /usr/lib/x86_64-linux-gnu/libc.so.6 (0x000071b737c00000)
	libGL.so.1 => /usr/lib/x86_64-linux-gnu/libGL.so.1 (0x000071b73c8c7000)
	libz.so.1 => /usr/lib/x86_64-linux-gnu/libz.so.1 (0x000071b73c8a9000)
	libicui18n.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicui18n.so.56 (0x000071b737600000)
	libicuuc.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicuuc.so.56 (0x000071b737200000)
	libicudata.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicudata.so.56 (0x000071b735800000)
	libdl.so.2 => /usr/lib/x86_64-linux-gnu/libdl.so.2 (0x000071b73c8a2000)
	libgthread-2.0.so.0 => /usr/lib/x86_64-linux-gnu/libgthread-2.0.so.0 (0x000071b73c89d000)
	libglib-2.0.so.0 => /usr/lib/x86_64-linux-gnu/libglib-2.0.so.0 (0x000071b737ea8000)
	/lib64/ld-linux-x86-64.so.2 (0x000071b73c99c000)
	libGLdispatch.so.0 => /usr/lib/x86_64-linux-gnu/libGLdispatch.so.0 (0x000071b738b47000)
	libGLX.so.0 => /usr/lib/x86_64-linux-gnu/libGLX.so.0 (0x000071b73c868000)
	libatomic.so.1 => /usr/lib/x86_64-linux-gnu/libatomic.so.1 (0x000071b73c85d000)
	libpcre2-8.so.0 => /usr/lib/x86_64-linux-gnu/libpcre2-8.so.0 (0x000071b737b54000)
	libX11.so.6 => /usr/lib/x86_64-linux-gnu/libX11.so.6 (0x000071b7356be000)
	libxcb.so.1 => /usr/lib/x86_64-linux-gnu/libxcb.so.1 (0x000071b7393d5000)
	libXau.so.6 => /usr/lib/x86_64-linux-gnu/libXau.so.6 (0x000071b7393cf000)
	libXdmcp.so.6 => /usr/lib/x86_64-linux-gnu/libXdmcp.so.6 (0x000071b7393c7000)
cg@cg-C1001140:~/Downloads/Firmware Upgrade Procedure from SE4SA531 to SE4SA550/PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux$ 


9/30/2026
[user@localhost PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux]$ nvme list
Node                  Generic               SN                   Model                                    Namespace  Usage                      Format           FW Rev  
--------------------- --------------------- -------------------- ---------------------------------------- ---------- -------------------------- ---------------- --------
/dev/nvme0n1          /dev/ng0n1            511221129056000360   DIGISTOR 2TB                             0x1          2.05  TB /   2.05  TB    512   B +  0 B   ECPG13.0
/dev/nvme1n1          /dev/ng1n1            7XT00AM8             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531
/dev/nvme2n1          /dev/ng2n1            7XT00ALD             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531
/dev/nvme3n1          /dev/ng3n1            7XT00AL8             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531
/dev/nvme4n1          /dev/ng4n1            7XT00AL5             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531

[user@localhost PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux]$ sudo ./PCIETOOL08-5890_DLMC\(Seagate\)\(SE4SA550\)_Linux_64bit AUTO
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys2/nvme2n1
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys1/nvme1n1
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys3/nvme3n1
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys4/nvme4n1
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys1/nvme1n1
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys1/nvme1n1
02 : S_R09
04 : A_F64
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys3/nvme3n1
01 : S_T17
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys2/nvme2n1
03 : A_F64
05 : A_F64
[MSG] change@/devices/virtual/nvme-subsystem/nvme-subsys4/nvme4n1
[user@localhost PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux]$ nvme list
Node                  Generic               SN                   Model                                    Namespace  Usage                      Format           FW Rev  
--------------------- --------------------- -------------------- ---------------------------------------- ---------- -------------------------- ---------------- --------
/dev/nvme0n1          /dev/ng0n1            511221129056000360   DIGISTOR 2TB                             0x1          2.05  TB /   2.05  TB    512   B +  0 B   ECPG13.0
/dev/nvme1n1          /dev/ng1n1            7XT00AM8             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA550
/dev/nvme2n1          /dev/ng2n1            7XT00ALD             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531
/dev/nvme3n1          /dev/ng3n1            7XT00AL8             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531
/dev/nvme4n1          /dev/ng4n1            7XT00AL5             XP12800LE70025                           0x1         12.80  TB /  12.80  TB    512   B +  0 B   SE4SA531


