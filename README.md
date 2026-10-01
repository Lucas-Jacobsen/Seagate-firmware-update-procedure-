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


9/30/2026 -
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

[user@localhost PCIETOOL08-5890_DLMC(Seagate)(SE4SA550)_Linux]$ ldd ./libMPFlow.so.1.0.0 
./libMPFlow.so.1.0.0: /lib64/libldap_r-2.4.so.2: no version information available (required by ./libMPFlow.so.1.0.0)
	linux-vdso.so.1 (0x00007ffeca3ab000)
	libldap_r-2.4.so.2 => /lib64/libldap_r-2.4.so.2 (0x00007f4471fbc000)
	libQt5Gui.so.5 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libQt5Gui.so.5 (0x00007f446e200000)
	libQt5Core.so.5 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libQt5Core.so.5 (0x00007f446da00000)
	libpthread.so.0 => /lib64/libpthread.so.0 (0x00007f4471fb7000)
	libstdc++.so.6 => /lib64/libstdc++.so.6 (0x00007f446d600000)
	libm.so.6 => /lib64/libm.so.6 (0x00007f4471eda000)
	libgcc_s.so.1 => /lib64/libgcc_s.so.1 (0x00007f4471ec0000)
	libc.so.6 => /lib64/libc.so.6 (0x00007f446d200000)
	libldap.so.2 => /lib64/libldap.so.2 (0x00007f4471e5a000)
	libGL.so.1 => /lib64/libGL.so.1 (0x00007f446e179000)
	libz.so.1 => /lib64/libz.so.1 (0x00007f446e9e6000)
	libicui18n.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicui18n.so.56 (0x00007f446cc00000)
	libicuuc.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicuuc.so.56 (0x00007f446c800000)
	libicudata.so.56 => /opt/Qt5.9.8/5.9.8/gcc_64/lib/libicudata.so.56 (0x00007f446ae00000)
	libdl.so.2 => /lib64/libdl.so.2 (0x00007f446e9df000)
	libgthread-2.0.so.0 => /lib64/libgthread-2.0.so.0 (0x00007f446e9da000)
	libglib-2.0.so.0 => /lib64/libglib-2.0.so.0 (0x00007f446d8c6000)
	/lib64/ld-linux-x86-64.so.2 (0x00007f4471fd2000)
	liblber.so.2 => /lib64/liblber.so.2 (0x00007f446e9c7000)
	libevent-2.1.so.7 => /lib64/libevent-2.1.so.7 (0x00007f446d86d000)
	libsasl2.so.3 => /lib64/libsasl2.so.3 (0x00007f446e159000)
	libssl.so.3 => /lib64/libssl.so.3 (0x00007f446d51a000)
	libcrypto.so.3 => /lib64/libcrypto.so.3 (0x00007f446a800000)
	libGLX.so.0 => /lib64/libGLX.so.0 (0x00007f446d83b000)
	libX11.so.6 => /lib64/libX11.so.6 (0x00007f446d0b8000)
	libXext.so.6 => /lib64/libXext.so.6 (0x00007f446d505000)
	libGLdispatch.so.0 => /lib64/libGLdispatch.so.0 (0x00007f446d44d000)
	libpcre.so.1 => /lib64/libpcre.so.1 (0x00007f446ad88000)
	libcrypt.so.2 => /lib64/libcrypt.so.2 (0x00007f446d413000)
	libgssapi_krb5.so.2 => /lib64/libgssapi_krb5.so.2 (0x00007f446ad32000)
	libkrb5.so.3 => /lib64/libkrb5.so.3 (0x00007f446a726000)
	libk5crypto.so.3 => /lib64/libk5crypto.so.3 (0x00007f446d09f000)
	libcom_err.so.2 => /lib64/libcom_err.so.2 (0x00007f446e9bc000)
	libresolv.so.2 => /lib64/libresolv.so.2 (0x00007f446cbec000)
	libxcb.so.1 => /lib64/libxcb.so.1 (0x00007f446cbc1000)
	libkrb5support.so.0 => /lib64/libkrb5support.so.0 (0x00007f446e148000)
	libkeyutils.so.1 => /lib64/libkeyutils.so.1 (0x00007f446e9b3000)
	libXau.so.6 => /lib64/libXau.so.6 (0x00007f446d835000)
	libselinux.so.1 => /lib64/libselinux.so.1 (0x00007f446a6f9000)
	libpcre2-8.so.0 => /lib64/libpcre2-8.so.0 (0x00007f446a65d000)


[user@localhost images]$ sudo sedutil-cli --query /dev/nvme1

/dev/nvme1 NVMe XP12800LE70025                           SE4SA550 7XT00AM8            
TPer function (0x0001)
    ACKNAK = N, ASYNC = N. BufferManagement = N, comIDManagement  = Y, Streaming = Y, SYNC = Y
Locking function (0x0002)
    Locked = N, LockingEnabled = N, LockingSupported = Y, MBRDone = N, MBREnabled = N, MediaEncrypt = Y
Geometry function (0x0003)
    Align = Y, Alignment Granularity = 8 (4096), Logical Block size = 512, Lowest Aligned LBA = 0
SingleUser function (0x0201)
    ALL = N, ANY = N, Policy = Y, Locking Objects = 9
DataStore function (0x0202)
    Max Tables = 9, Max Size Tables = 10485760, Table size alignment = 1
OPAL 2.0 function (0x0203)
    Base comID = 0x1000, Initial PIN = 0x00, Reverted PIN = 0x00, comIDs = 1
    Locking Admins = 4, Locking Users = 9, Range Crossing = N

TPer Properties: 
  MaxComPacketSize = 16384  MaxResponseComPacketSize = 16384
  MaxPacketSize = 16364  MaxIndTokenSize = 16328  MaxPackets = 1
  MaxSubpackets = 1  MaxMethods = 1  MaxSessions = 1
  MaxAuthentications = 13  MaxTransactionLimit = 1  DefSessionTimeout = 0
  MaxSessionTimeout = 0  MinSessionTimeout = 0
Host Properties: 

  MaxComPacketSize = 2048  MaxResponseComPacketSize = 2048  MaxPacketSize = 2028
  MaxIndTokenSize = 1992  MaxPackets = 1  MaxSubpackets = 1
  MaxMethods = 1

[user@localhost images]$ 


[user@localhost images]$ sudo sedutil-cli --scan
Scanning for Opal compliant disks
/dev/nvme0  2  DIGISTOR 2TB                             ECPG13.0
/dev/nvme1  2  XP12800LE70025                           SE4SA550
/dev/nvme2  2  XP12800LE70025                           SE4SA531
/dev/nvme3  2  XP12800LE70025                           SE4SA531
/dev/nvme4  2  XP12800LE70025                           SE4SA531
The Kernel flag libata.allow_tpm is not set correctly
Please see the readme note about setting the libata.allow_tpm 
/dev/sda   No   
No more disks present ending scan
[user@localhost images]$ sudo sedutil-cli --query /dev/nvme2  

/dev/nvme2 NVMe XP12800LE70025                           SE4SA531 7XT00ALD            
TPer function (0x0001)
    ACKNAK = N, ASYNC = N. BufferManagement = N, comIDManagement  = Y, Streaming = Y, SYNC = Y
Locking function (0x0002)
    Locked = N, LockingEnabled = Y, LockingSupported = Y, MBRDone = N, MBREnabled = N, MediaEncrypt = Y
Geometry function (0x0003)
    Align = Y, Alignment Granularity = 8 (32768), Logical Block size = 4096, Lowest Aligned LBA = 0
SingleUser function (0x0201)
    ALL = N, ANY = N, Policy = Y, Locking Objects = 9
DataStore function (0x0202)
    Max Tables = 9, Max Size Tables = 10485760, Table size alignment = 1
OPAL 2.0 function (0x0203)
    Base comID = 0x1000, Initial PIN = 0x00, Reverted PIN = 0x00, comIDs = 1
    Locking Admins = 4, Locking Users = 9, Range Crossing = N

TPer Properties: 
  MaxComPacketSize = 16384  MaxResponseComPacketSize = 16384
  MaxPacketSize = 16364  MaxIndTokenSize = 16328  MaxPackets = 1
  MaxSubpackets = 1  MaxMethods = 1  MaxSessions = 1
  MaxAuthentications = 2  MaxTransactionLimit = 1  DefSessionTimeout = 0
  MaxSessionTimeout = 0  MinSessionTimeout = 0
Host Properties: 

  MaxComPacketSize = 2048  MaxResponseComPacketSize = 2048  MaxPacketSize = 2028
  MaxIndTokenSize = 1992  MaxPackets = 1  MaxSubpackets = 1
  MaxMethods = 1

[user@localhost images]$ 


