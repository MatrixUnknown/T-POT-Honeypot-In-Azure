$ ssh student@myipaddress
The authenticity of host myipaddress (myipaddress)' can't be established.
ED25519 key fingerprint is SHA256:FO+Vi+YLLyVuAraRFmqT6S+/h62rxA2ieu+mRCqAgO0.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'myipaddress' (ED25519) to the list of known hosts.
password: 
Linux tpot-debian 6.1.0-23-cloud-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.99-1 (2024-07-15) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
$ git clone https://github.com/telekom-security/tpotce
student@tpot-debian:~$ sudo apt update
Get:1 file:/etc/apt/mirrors/debian.list Mirrorlist [37 B]
Get:4 file:/etc/apt/mirrors/debian-security.list Mirrorlist [46 B]
Get:2 http://azure.deb.debian.cloud/debian bookworm InRelease [151 kB]
Get:3 http://azure.deb.debian.cloud/debian bookworm-updates InRelease [55.4 kB]
Get:5 http://azure.deb.debian.cloud/debian bookworm-backports InRelease [59.0 kB]
Get:6 http://azure.deb.debian.cloud/debian-security bookworm-security InRelease [48.0 kB]
Get:7 http://azure.deb.debian.cloud/debian bookworm/main Sources [9487 kB]
Get:8 http://azure.deb.debian.cloud/debian bookworm/main amd64 Packages [8787 kB]
Get:9 http://azure.deb.debian.cloud/debian bookworm/main Translation-en [6109 kB]
Get:10 http://azure.deb.debian.cloud/debian bookworm-updates/main Sources [1260 B]
Get:11 http://azure.deb.debian.cloud/debian bookworm-updates/main amd64 Packages [2468 B]
Get:12 http://azure.deb.debian.cloud/debian bookworm-updates/main Translation-en [2928 B]
Get:13 http://azure.deb.debian.cloud/debian bookworm-backports/main Sources [272 kB]
Get:14 http://azure.deb.debian.cloud/debian bookworm-backports/main amd64 Packages [239 kB]
Get:15 http://azure.deb.debian.cloud/debian bookworm-backports/main Translation-en [201 kB]
Get:16 http://azure.deb.debian.cloud/debian-security bookworm-security/main Sources [110 kB]
Get:17 http://azure.deb.debian.cloud/debian-security bookworm-security/main amd64 Packages [182 kB]
Get:18 http://azure.deb.debian.cloud/debian-security bookworm-security/main Translation-en [110 kB]
Fetched 25.8 MB in 4s (6786 kB/s)                               
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
35 packages can be upgraded. Run 'apt list --upgradable' to see them.
$ sudo apt install git
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  git-man liberror-perl libgdbm-compat4 libperl5.36 patch perl perl-modules-5.36
Suggested packages:
  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn ed
  diffutils-doc perl-doc libterm-readline-gnu-perl | libterm-readline-perl-perl make libtap-harness-archive-perl
The following NEW packages will be installed:
  git git-man liberror-perl libgdbm-compat4 libperl5.36 patch perl perl-modules-5.36
0 upgraded, 8 newly installed, 0 to remove and 35 not upgraded.
Need to get 16.8 MB of archives.
After this operation, 97.0 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 file:/etc/apt/mirrors/debian.list Mirrorlist [37 B]
Get:2 file:/etc/apt/mirrors/debian-security.list Mirrorlist [46 B]
Get:3 http://azure.deb.debian.cloud/debian bookworm/main amd64 perl-modules-5.36 all 5.36.0-7+deb12u1 [2815 kB]
Get:4 http://azure.deb.debian.cloud/debian bookworm/main amd64 libgdbm-compat4 amd64 1.23-3 [48.2 kB]
Get:5 http://azure.deb.debian.cloud/debian bookworm/main amd64 libperl5.36 amd64 5.36.0-7+deb12u1 [4218 kB]
Get:6 http://azure.deb.debian.cloud/debian bookworm/main amd64 perl amd64 5.36.0-7+deb12u1 [239 kB]
Get:7 http://azure.deb.debian.cloud/debian bookworm/main amd64 liberror-perl all 0.17029-2 [29.0 kB]
Get:8 http://azure.deb.debian.cloud/debian bookworm/main amd64 patch amd64 2.7.6-7 [128 kB]
Get:9 http://azure.deb.debian.cloud/debian-security bookworm-security/main amd64 git-man all 1:2.39.5-0+deb12u1 [2054 kB]
Get:10 http://azure.deb.debian.cloud/debian-security bookworm-security/main amd64 git amd64 1:2.39.5-0+deb12u1 [7256 kB]
Fetched 16.8 MB in 0s (57.4 MB/s)
Selecting previously unselected package perl-modules-5.36.
(Reading database ... 20978 files and directories currently installed.)
Preparing to unpack .../0-perl-modules-5.36_5.36.0-7+deb12u1_all.deb ...
Unpacking perl-modules-5.36 (5.36.0-7+deb12u1) ...
Selecting previously unselected package libgdbm-compat4:amd64.
Preparing to unpack .../1-libgdbm-compat4_1.23-3_amd64.deb ...
Unpacking libgdbm-compat4:amd64 (1.23-3) ...
Selecting previously unselected package libperl5.36:amd64.
Preparing to unpack .../2-libperl5.36_5.36.0-7+deb12u1_amd64.deb ...
Unpacking libperl5.36:amd64 (5.36.0-7+deb12u1) ...
Selecting previously unselected package perl.
Preparing to unpack .../3-perl_5.36.0-7+deb12u1_amd64.deb ...
Unpacking perl (5.36.0-7+deb12u1) ...
Selecting previously unselected package liberror-perl.
Preparing to unpack .../4-liberror-perl_0.17029-2_all.deb ...
Unpacking liberror-perl (0.17029-2) ...
Selecting previously unselected package git-man.
Preparing to unpack .../5-git-man_1%3a2.39.5-0+deb12u1_all.deb ...
Unpacking git-man (1:2.39.5-0+deb12u1) ...
Selecting previously unselected package git.
Preparing to unpack .../6-git_1%3a2.39.5-0+deb12u1_amd64.deb ...
Unpacking git (1:2.39.5-0+deb12u1) ...
Selecting previously unselected package patch.
Preparing to unpack .../7-patch_2.7.6-7_amd64.deb ...
Unpacking patch (2.7.6-7) ...
Setting up perl-modules-5.36 (5.36.0-7+deb12u1) ...
Setting up patch (2.7.6-7) ...
Setting up libgdbm-compat4:amd64 (1.23-3) ...
Setting up git-man (1:2.39.5-0+deb12u1) ...
Setting up libperl5.36:amd64 (5.36.0-7+deb12u1) ...
Setting up perl (5.36.0-7+deb12u1) ...
Setting up liberror-perl (0.17029-2) ...
Setting up git (1:2.39.5-0+deb12u1) ...
Processing triggers for man-db (2.11.2-2) ...
Processing triggers for libc-bin (2.36-9+deb12u7) ...
student@tpot-debian:~$ git version
git version 2.39.5
student@tpot-debian:~$ git clone https://github.com/telekom-security/tpotce
Cloning into 'tpotce'...
remote: Enumerating objects: 16385, done.
remote: Counting objects: 100% (397/397), done.
remote: Compressing objects: 100% (285/285), done.
remote: Total 16385 (delta 150), reused 324 (delta 109), pack-reused 15988 (from 1)
Receiving objects: 100% (16385/16385), 281.18 MiB | 39.31 MiB/s, done.
Resolving deltas: 100% (9071/9071), done.
student@tpot-debian:~$ cd tpotce
student@tpot-debian:~/tpotce$ ./install.sh
 _____     ____       _      ___           _        _ _
|_   _|   |  _ \ ___ | |_   |_ _|_ __  ___| |_ __ _| | | ___ _ __
  | |_____| |_) / _ \| __|   | || '_ \/ __| __/ _` | | |/ _ \ '__|
  | |_____|  __/ (_) | |_    | || | | \__ \ || (_| | | |  __/ |
  |_|     |_|   \___/ \__|  |___|_| |_|___/\__\__,_|_|_|\___|_|


### This script will now install T-Pot and all of its dependencies.

### Install? (y/n) y


### Now installing required packages ...

Get:1 file:/etc/apt/mirrors/debian.list Mirrorlist [37 B]
Get:2 file:/etc/apt/mirrors/debian-security.list Mirrorlist [46 B]
Hit:3 http://azure.deb.debian.cloud/debian bookworm InRelease
Hit:4 http://azure.deb.debian.cloud/debian bookworm-updates InRelease
Hit:5 http://azure.deb.debian.cloud/debian bookworm-backports InRelease
Hit:6 http://azure.deb.debian.cloud/debian-security bookworm-security InRelease
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
35 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
wget is already the newest version (1.21.3-1+b2).
wget set to manually installed.
The following additional packages will be installed:
  ansible-core ieee-data libapr1 libaprutil1 libcrack2 python3-anyio python3-argcomplete python3-click
  python3-colorama python3-distutils python3-dnspython python3-h11 python3-h2 python3-hpack python3-httpcore
  python3-httpx python3-hyperframe python3-jmespath python3-kerberos python3-lib2to3 python3-libcloud
  python3-lockfile python3-netaddr python3-ntlm-auth python3-packaging python3-passlib python3-requests-kerberos
  python3-requests-ntlm python3-requests-toolbelt python3-resolvelib python3-rfc3986 python3-selinux
  python3-simplejson python3-sniffio python3-winrm python3-xmltodict wamerican
Suggested packages:
  cowsay sshpass python3-trio python3-aioquic python-lockfile-doc ipython3 python-netaddr-docs
The following NEW packages will be installed:
  ansible ansible-core apache2-utils cracklib-runtime ieee-data libapr1 libaprutil1 libcrack2 python3-anyio
  python3-argcomplete python3-click python3-colorama python3-distutils python3-dnspython python3-h11 python3-h2
  python3-hpack python3-httpcore python3-httpx python3-hyperframe python3-jmespath python3-kerberos python3-lib2to3
  python3-libcloud python3-lockfile python3-netaddr python3-ntlm-auth python3-packaging python3-passlib
  python3-requests-kerberos python3-requests-ntlm python3-requests-toolbelt python3-resolvelib python3-rfc3986
  python3-selinux python3-simplejson python3-sniffio python3-winrm python3-xmltodict wamerican
0 upgraded, 40 newly installed, 0 to remove and 35 not upgraded.
Need to get 23.9 MB of archives.
After this operation, 308 MB of additional disk space will be used.
Get:1 file:/etc/apt/mirrors/debian.list Mirrorlist [37 B]
Get:2 http://azure.deb.debian.cloud/debian bookworm/main amd64 wamerican all 2020.12.07-2 [221 kB]
Get:3 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-packaging all 23.0-1 [32.5 kB]
Get:4 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-resolvelib all 0.9.0-2 [27.3 kB]
Get:5 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-lib2to3 all 3.11.2-3 [76.3 kB]
Get:6 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-distutils all 3.11.2-3 [131 kB]
Get:7 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-dnspython all 2.3.0-1 [152 kB]
Get:8 http://azure.deb.debian.cloud/debian bookworm/main amd64 ieee-data all 20220827.1 [2029 kB]
Get:9 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-netaddr all 0.8.0-2 [295 kB]
Get:10 http://azure.deb.debian.cloud/debian bookworm/main amd64 ansible-core all 2.14.16-0+deb12u1 [1289 kB]
Get:11 http://azure.deb.debian.cloud/debian bookworm/main amd64 ansible all 7.7.0+dfsg-3+deb12u1 [16.9 MB]
Get:12 http://azure.deb.debian.cloud/debian bookworm/main amd64 libapr1 amd64 1.7.2-3 [102 kB]
Get:13 http://azure.deb.debian.cloud/debian bookworm/main amd64 libaprutil1 amd64 1.6.3-1 [87.8 kB]
Get:14 http://azure.deb.debian.cloud/debian bookworm/main amd64 apache2-utils amd64 2.4.62-1~deb12u1 [210 kB]
Get:15 http://azure.deb.debian.cloud/debian bookworm/main amd64 libcrack2 amd64 2.9.6-5+b1 [44.0 kB]
Get:16 http://azure.deb.debian.cloud/debian bookworm/main amd64 cracklib-runtime amd64 2.9.6-5+b1 [143 kB]
Get:17 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-sniffio all 1.2.0-1 [6372 B]
Get:18 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-anyio all 3.6.2-1 [54.0 kB]
Get:19 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-argcomplete all 2.0.0-1 [34.7 kB]
Get:20 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-colorama all 0.4.6-2 [36.8 kB]
Get:21 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-click all 8.1.3-2 [92.2 kB]
Get:22 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-h11 all 0.14.0-1 [50.1 kB]
Get:23 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-hpack all 4.0.0-2 [25.0 kB]
Get:24 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-hyperframe all 6.0.0-1 [14.5 kB]
Get:25 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-h2 all 4.1.0-4 [80.8 kB]
Get:26 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-httpcore all 0.16.3-1 [38.4 kB]
Get:27 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-rfc3986 all 1.5.0-2 [22.2 kB]
Get:28 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-httpx all 0.23.3-1 [72.3 kB]
Get:29 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-jmespath all 1.0.1-1 [21.1 kB]
Get:30 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-kerberos amd64 1.1.14-3.1+b7 [21.5 kB]
Get:31 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-lockfile all 1:0.12.2-2.2 [17.3 kB]
Get:32 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-simplejson amd64 3.18.3-1 [59.8 kB]
Get:33 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-libcloud all 3.4.1-5 [808 kB]
Get:34 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-ntlm-auth all 1.4.0-2 [21.9 kB]
Get:35 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-passlib all 1.7.4-3 [367 kB]
Get:36 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-requests-kerberos all 0.12.0-2 [13.0 kB]
Get:37 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-requests-ntlm all 1.1.0-3 [6268 B]
Get:38 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-requests-toolbelt all 0.10.1-1 [41.3 kB]
Get:39 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-selinux amd64 3.4-1+b6 [152 kB]
Get:40 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-xmltodict all 0.13.0-1 [16.7 kB]
Get:41 http://azure.deb.debian.cloud/debian bookworm/main amd64 python3-winrm all 0.3.0-4+deb12u1 [22.1 kB]
Fetched 23.9 MB in 0s (61.6 MB/s)           
Extracting templates from packages: 100%
Preconfiguring packages ...
Selecting previously unselected package wamerican.
(Reading database ... 24095 files and directories currently installed.)
Preparing to unpack .../00-wamerican_2020.12.07-2_all.deb ...
Unpacking wamerican (2020.12.07-2) ...
Selecting previously unselected package python3-packaging.
Preparing to unpack .../01-python3-packaging_23.0-1_all.deb ...
Unpacking python3-packaging (23.0-1) ...
Selecting previously unselected package python3-resolvelib.
Preparing to unpack .../02-python3-resolvelib_0.9.0-2_all.deb ...
Unpacking python3-resolvelib (0.9.0-2) ...
Selecting previously unselected package python3-lib2to3.
Preparing to unpack .../03-python3-lib2to3_3.11.2-3_all.deb ...
Unpacking python3-lib2to3 (3.11.2-3) ...
Selecting previously unselected package python3-distutils.
Preparing to unpack .../04-python3-distutils_3.11.2-3_all.deb ...
Unpacking python3-distutils (3.11.2-3) ...
Selecting previously unselected package python3-dnspython.
Preparing to unpack .../05-python3-dnspython_2.3.0-1_all.deb ...
Unpacking python3-dnspython (2.3.0-1) ...
Selecting previously unselected package ieee-data.
Preparing to unpack .../06-ieee-data_20220827.1_all.deb ...
Unpacking ieee-data (20220827.1) ...
Selecting previously unselected package python3-netaddr.
Preparing to unpack .../07-python3-netaddr_0.8.0-2_all.deb ...
Unpacking python3-netaddr (0.8.0-2) ...
Selecting previously unselected package ansible-core.
Preparing to unpack .../08-ansible-core_2.14.16-0+deb12u1_all.deb ...
Unpacking ansible-core (2.14.16-0+deb12u1) ...
Selecting previously unselected package ansible.
Preparing to unpack .../09-ansible_7.7.0+dfsg-3+deb12u1_all.deb ...
Unpacking ansible (7.7.0+dfsg-3+deb12u1) ...
Selecting previously unselected package libapr1:amd64.
Preparing to unpack .../10-libapr1_1.7.2-3_amd64.deb ...
Unpacking libapr1:amd64 (1.7.2-3) ...
Selecting previously unselected package libaprutil1:amd64.
Preparing to unpack .../11-libaprutil1_1.6.3-1_amd64.deb ...
Unpacking libaprutil1:amd64 (1.6.3-1) ...
Selecting previously unselected package apache2-utils.
Preparing to unpack .../12-apache2-utils_2.4.62-1~deb12u1_amd64.deb ...
Unpacking apache2-utils (2.4.62-1~deb12u1) ...
Selecting previously unselected package libcrack2:amd64.
Preparing to unpack .../13-libcrack2_2.9.6-5+b1_amd64.deb ...
Unpacking libcrack2:amd64 (2.9.6-5+b1) ...
Selecting previously unselected package cracklib-runtime.
Preparing to unpack .../14-cracklib-runtime_2.9.6-5+b1_amd64.deb ...
Unpacking cracklib-runtime (2.9.6-5+b1) ...
Selecting previously unselected package python3-sniffio.
Preparing to unpack .../15-python3-sniffio_1.2.0-1_all.deb ...
Unpacking python3-sniffio (1.2.0-1) ...
Selecting previously unselected package python3-anyio.
Preparing to unpack .../16-python3-anyio_3.6.2-1_all.deb ...
Unpacking python3-anyio (3.6.2-1) ...
Selecting previously unselected package python3-argcomplete.
Preparing to unpack .../17-python3-argcomplete_2.0.0-1_all.deb ...
Unpacking python3-argcomplete (2.0.0-1) ...
Selecting previously unselected package python3-colorama.
Preparing to unpack .../18-python3-colorama_0.4.6-2_all.deb ...
Unpacking python3-colorama (0.4.6-2) ...
Selecting previously unselected package python3-click.
Preparing to unpack .../19-python3-click_8.1.3-2_all.deb ...
Unpacking python3-click (8.1.3-2) ...
Selecting previously unselected package python3-h11.
Preparing to unpack .../20-python3-h11_0.14.0-1_all.deb ...
Unpacking python3-h11 (0.14.0-1) ...
Selecting previously unselected package python3-hpack.
Preparing to unpack .../21-python3-hpack_4.0.0-2_all.deb ...
Unpacking python3-hpack (4.0.0-2) ...
Selecting previously unselected package python3-hyperframe.
Preparing to unpack .../22-python3-hyperframe_6.0.0-1_all.deb ...
Unpacking python3-hyperframe (6.0.0-1) ...
Selecting previously unselected package python3-h2.
Preparing to unpack .../23-python3-h2_4.1.0-4_all.deb ...
Unpacking python3-h2 (4.1.0-4) ...
Selecting previously unselected package python3-httpcore.
Preparing to unpack .../24-python3-httpcore_0.16.3-1_all.deb ...
Unpacking python3-httpcore (0.16.3-1) ...
Selecting previously unselected package python3-rfc3986.
Preparing to unpack .../25-python3-rfc3986_1.5.0-2_all.deb ...
Unpacking python3-rfc3986 (1.5.0-2) ...
Selecting previously unselected package python3-httpx.
Preparing to unpack .../26-python3-httpx_0.23.3-1_all.deb ...
Unpacking python3-httpx (0.23.3-1) ...
Selecting previously unselected package python3-jmespath.
Preparing to unpack .../27-python3-jmespath_1.0.1-1_all.deb ...
Unpacking python3-jmespath (1.0.1-1) ...
Selecting previously unselected package python3-kerberos.
Preparing to unpack .../28-python3-kerberos_1.1.14-3.1+b7_amd64.deb ...
Unpacking python3-kerberos (1.1.14-3.1+b7) ...
Selecting previously unselected package python3-lockfile.
Preparing to unpack .../29-python3-lockfile_1%3a0.12.2-2.2_all.deb ...
Unpacking python3-lockfile (1:0.12.2-2.2) ...
Selecting previously unselected package python3-simplejson.
Preparing to unpack .../30-python3-simplejson_3.18.3-1_amd64.deb ...
Unpacking python3-simplejson (3.18.3-1) ...
Selecting previously unselected package python3-libcloud.
Preparing to unpack .../31-python3-libcloud_3.4.1-5_all.deb ...
Unpacking python3-libcloud (3.4.1-5) ...
Selecting previously unselected package python3-ntlm-auth.
Preparing to unpack .../32-python3-ntlm-auth_1.4.0-2_all.deb ...
Unpacking python3-ntlm-auth (1.4.0-2) ...
Selecting previously unselected package python3-passlib.
Preparing to unpack .../33-python3-passlib_1.7.4-3_all.deb ...
Unpacking python3-passlib (1.7.4-3) ...
Selecting previously unselected package python3-requests-kerberos.
Preparing to unpack .../34-python3-requests-kerberos_0.12.0-2_all.deb ...
Unpacking python3-requests-kerberos (0.12.0-2) ...
Selecting previously unselected package python3-requests-ntlm.
Preparing to unpack .../35-python3-requests-ntlm_1.1.0-3_all.deb ...
Unpacking python3-requests-ntlm (1.1.0-3) ...
Selecting previously unselected package python3-requests-toolbelt.
Preparing to unpack .../36-python3-requests-toolbelt_0.10.1-1_all.deb ...
Unpacking python3-requests-toolbelt (0.10.1-1) ...
Selecting previously unselected package python3-selinux.
Preparing to unpack .../37-python3-selinux_3.4-1+b6_amd64.deb ...
Unpacking python3-selinux (3.4-1+b6) ...
Selecting previously unselected package python3-xmltodict.
Preparing to unpack .../38-python3-xmltodict_0.13.0-1_all.deb ...
Unpacking python3-xmltodict (0.13.0-1) ...
Selecting previously unselected package python3-winrm.
Preparing to unpack .../39-python3-winrm_0.3.0-4+deb12u1_all.deb ...
Unpacking python3-winrm (0.3.0-4+deb12u1) ...
Setting up python3-sniffio (1.2.0-1) ...
Setting up python3-lockfile (1:0.12.2-2.2) ...
Setting up python3-requests-toolbelt (0.10.1-1) ...
Setting up python3-passlib (1.7.4-3) ...
Setting up python3-anyio (3.6.2-1) ...
Setting up python3-hyperframe (6.0.0-1) ...
Setting up python3-hpack (4.0.0-2) ...
Setting up python3-colorama (0.4.6-2) ...
Setting up python3-ntlm-auth (1.4.0-2) ...
Setting up python3-resolvelib (0.9.0-2) ...
Setting up libapr1:amd64 (1.7.2-3) ...
Setting up python3-kerberos (1.1.14-3.1+b7) ...
Setting up python3-click (8.1.3-2) ...
Setting up python3-simplejson (3.18.3-1) ...
Setting up python3-xmltodict (0.13.0-1) ...
Setting up python3-packaging (23.0-1) ...
Setting up python3-rfc3986 (1.5.0-2) ...
Setting up python3-jmespath (1.0.1-1) ...
Setting up wamerican (2020.12.07-2) ...
Setting up python3-h11 (0.14.0-1) ...
Setting up libcrack2:amd64 (2.9.6-5+b1) ...
Setting up python3-requests-kerberos (0.12.0-2) ...
Setting up ieee-data (20220827.1) ...
Setting up python3-dnspython (2.3.0-1) ...
Setting up python3-selinux (3.4-1+b6) ...
Setting up python3-h2 (4.1.0-4) ...
Setting up python3-argcomplete (2.0.0-1) ...
Setting up python3-lib2to3 (3.11.2-3) ...
Setting up libaprutil1:amd64 (1.6.3-1) ...
Setting up python3-distutils (3.11.2-3) ...
Setting up python3-httpcore (0.16.3-1) ...
Setting up python3-requests-ntlm (1.1.0-3) ...
Setting up python3-libcloud (3.4.1-5) ...
Setting up cracklib-runtime (2.9.6-5+b1) ...
Setting up python3-httpx (0.23.3-1) ...
Setting up python3-netaddr (0.8.0-2) ...
Setting up python3-winrm (0.3.0-4+deb12u1) ...
Setting up apache2-utils (2.4.62-1~deb12u1) ...
Setting up ansible-core (2.14.16-0+deb12u1) ...
Setting up ansible (7.7.0+dfsg-3+deb12u1) ...
Processing triggers for man-db (2.11.2-2) ...
Processing triggers for libc-bin (2.36-9+deb12u7) ...

### Using local T-Pot Ansible Installation Playbook ... 
### ‘sudo‘ acquired, setting ansible become option to --become.

### Now running T-Pot Ansible Installation Playbook ...


PLAY [T-Pot - Bootstrapping Python] *********************************************************************************

TASK [Get distribution name (All)] **********************************************************************************
changed: [127.0.0.1]

TASK [Check if python3 is installed (All)] **************************************************************************
changed: [127.0.0.1]

TASK [Add python package (Debian, Raspbian, Ubuntu)] ****************************************************************
skipping: [127.0.0.1]

PLAY [T-Pot - Abort if run as tpot, root or on unsupported distribution] ********************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Check if running as root (All)] *******************************************************************************
ok: [127.0.0.1] => {
    "changed": false,
    "msg": "Running as user: student."
}

TASK [Check if running as tpot (All)] *******************************************************************************
ok: [127.0.0.1] => {
    "changed": false,
    "msg": "Running as user: student."
}

TASK [Check if supported distribution (All)] ************************************************************************
ok: [127.0.0.1] => {
    "changed": false,
    "msg": "T-Pot will now install on Debian."
}

PLAY [T-Pot - Install recommended, remove conflicting packages] *****************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Syncing clocks (All)] *****************************************************************************************
fatal: [127.0.0.1]: FAILED! => {"changed": true, "cmd": "hwclock --hctosys", "delta": "0:00:10.069283", "end": "2024-09-17 22:59:15.869754", "msg": "non-zero return code", "rc": 1, "start": "2024-09-17 22:59:05.800471", "stderr": "hwclock: select() to /dev/rtc0 to wait for clock tick timed out", "stderr_lines": ["hwclock: select() to /dev/rtc0 to wait for clock tick timed out"], "stdout": "", "stdout_lines": []}
...ignoring

TASK [Install recommended packages (Debian, Raspbian, Ubuntu)] ******************************************************
changed: [127.0.0.1]

TASK [Install exa (Debian, Raspbian, Ubuntu)] ***********************************************************************
changed: [127.0.0.1]

TASK [Install eza (if exa failed)] **********************************************************************************
skipping: [127.0.0.1]

PLAY [T-Pot - Prepare for and install Docker Engine] ****************************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Remove distribution based Docker packages and podman-docker (AlmaLinux, Debian, Fedora, Raspbian, Rocky, Ubuntu)] ***
ok: [127.0.0.1]

TASK [Add folder for Docker Engine GPG key (Debian, Raspbian, Ubuntu)] **********************************************
ok: [127.0.0.1]

TASK [Download Docker Engine GPG key (Debian, Raspbian, Ubuntu)] ****************************************************
changed: [127.0.0.1]

TASK [Decrypt Docker Engine GPG key (Debian, Raspbian, Ubuntu)] *****************************************************
changed: [127.0.0.1]

TASK [Add Docker Engine repository (Debian, Raspbian, Ubuntu)] ******************************************************
changed: [127.0.0.1]

PLAY [T-Pot - Install Docker Engine] ********************************************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Install Docker Engine packages (AlmaLinux, Debian, Fedora, Raspbian, Rocky, Ubuntu)] **************************
changed: [127.0.0.1]

TASK [Stop Docker (All)] ********************************************************************************************
changed: [127.0.0.1]

PLAY [T-Pot - Adjust configs, add users and groups, etc.] ***********************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Create T-Pot group (All)] *************************************************************************************
changed: [127.0.0.1]

TASK [Create T-Pot user (All)] **************************************************************************************
changed: [127.0.0.1]

TASK [Change SSH Port to 64295 (AlmaLinux, Debian, Fedora, Raspbian, Rocky, Ubuntu)] ********************************
changed: [127.0.0.1]

PLAY [T-Pot - Restart services] *************************************************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Enable Docker Engine upon boot (All)] *************************************************************************
changed: [127.0.0.1]

TASK [Restart SSH (All)] ********************************************************************************************
changed: [127.0.0.1]

PLAY [T-Pot - Adjust group users, bashrc, clone / update T-Pot repository] ******************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Check for non-root user id (All)] *****************************************************************************
ok: [127.0.0.1] => {
    "msg": "Detected user: 'student'"
}

TASK [Add aliases with exa (All)] ***********************************************************************************
changed: [127.0.0.1]

TASK [Add aliases with eza (Debian, Raspbian, Ubuntu)] **************************************************************
skipping: [127.0.0.1]

TASK [Clone / Update T-Pot repository (All)] ************************************************************************
ok: [127.0.0.1]

TASK [Add current user to Docker, T-Pot group (All)] ****************************************************************
changed: [127.0.0.1]

PLAY [T-Pot - Install service] **************************************************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Install systemd service (All)] ********************************************************************************
changed: [127.0.0.1]

RUNNING HANDLER [Reload systemd and enable service] *****************************************************************
changed: [127.0.0.1]

PLAY [T-Pot - Setup a randomized daily reboot] **********************************************************************

TASK [Gathering Facts] **********************************************************************************************
ok: [127.0.0.1]

TASK [Setup a randomized daily reboot (All)] ************************************************************************
changed: [127.0.0.1]

PLAY RECAP **********************************************************************************************************
127.0.0.1                  : ok=36   changed=20   unreachable=0    failed=0    skipped=3    rescued=0    ignored=1   

### Playbook was successful.


### Choose your T-Pot type:
### (H)ive   - T-Pot Standard / HIVE installation.
###            Includes also everything you need for a distributed setup with sensors.
### (S)ensor - T-Pot Sensor installation.
###            Optimized for a distributed installation, without WebUI, Elasticsearch and Kibana.
### (M)obile - T-Pot Mobile installation.
###            Includes everything to run T-Pot Mobile (available separately).
### Install Type? (h/s/m) h

### Installing T-Pot Standard / HIVE.

### T-Pot User Configuration ...

### Enter your web user name: Matrix_Prodigy
### Your username is: Matrix_Prodigy
### Is this correct? (y/n) y

### Enter password for your web user: 
### Repeat password you your web user: 
### Passwords do not match.

### Enter password for your web user: 
### Repeat password you your web user: 
### Creating base64 encoded htpasswd username and password for T-Pot config file: /home/student/tpotce/.env

### Now pulling images ...
[+] Pulling 112/38
 ✔ tanner_api Skipped - Image is already being pulled by tanner                                                 0.0s 
 ✔ map_redis Skipped - Image is already being pulled by tanner_redis                                            0.0s 
 ✔ conpot_ipmi Skipped - Image is already being pulled by conpot_kamstrup_382                                   0.0s 
 ✔ conpot_IEC104 Skipped - Image is already being pulled by conpot_kamstrup_382                                 0.0s 
 ✔ map_data Skipped - Image is already being pulled by map_web                                                  0.0s 
 ✔ conpot_guardian_ast Skipped - Image is already being pulled by conpot_kamstrup_382                           0.0s 
 ✔ p0f Pulled                                                                                                  11.2s 
 ✔ adbhoney Pulled                                                                                             30.4s 
 ✔ ddospot Pulled                                                                                             107.9s 
 ✔ tanner Pulled                                                                                               97.9s 
 ✔ citrixhoneypot Pulled                                                                                       45.3s 
 ✔ kibana Pulled                                                                                              171.2s 
 ✔ snare Pulled                                                                                                70.2s 
 ✔ spiderfoot Pulled                                                                                          129.4s 
 ✔ elasticsearch Pulled                                                                                       159.0s 
 ✔ ciscoasa Pulled                                                                                             97.8s 
 ✔ map_web Pulled                                                                                              35.2s 
 ✔ ipphoney Pulled                                                                                            102.2s 
 ✔ nginx Pulled                                                                                                26.3s 
 ✔ conpot_kamstrup_382 Pulled                                                                                 110.7s 
 ✔ ewsposter Pulled                                                                                            97.6s 
 ✔ fatt Pulled                                                                                                107.8s 
 ✔ wordpot Pulled                                                                                              42.0s 
 ✔ tanner_phpox Pulled                                                                                         51.2s 
 ✔ tpotinit Pulled                                                                                             27.2s 
 ✔ heralding Pulled                                                                                            78.5s 
 ✔ cowrie Pulled                                                                                               70.0s 
 ✔ honeytrap Pulled                                                                                           104.0s 
 ✔ tanner_redis Pulled                                                                                         22.2s 
 ✔ mailoney Pulled                                                                                             45.8s 
 ✔ dicompot Pulled                                                                                             19.9s 
 ✔ suricata Pulled                                                                                             80.9s 
 ✔ redishoneypot Pulled                                                                                        43.1s 
 ✔ sentrypeer Pulled                                                                                           70.5s 
 ✔ medpot Pulled                                                                                               21.0s 
 ✔ logstash Pulled                                                                                            146.5s 
 ✔ dionaea Pulled                                                                                             100.6s 
 ✔ elasticpot Pulled                                                                                          108.8s 

### Please review for possible honeypot port conflicts.
### While SSH is taken care of, other services such as
### SMTP, HTTP, etc. might prevent T-Pot from starting.

Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       User       Inode      PID/Program name    
tcp        0      0 127.0.0.54:53           0.0.0.0:*               LISTEN      997        13449      433/systemd-resolve 
tcp        0      0 0.0.0.0:64295           0.0.0.0:*               LISTEN      0          32484      6637/sshd: /usr/sbi 
tcp        0      0 0.0.0.0:5355            0.0.0.0:*               LISTEN      997        13435      433/systemd-resolve 
tcp        0      0 127.0.0.53:53           0.0.0.0:*               LISTEN      997        13447      433/systemd-resolve 
tcp        0      0 127.0.0.1:25            0.0.0.0:*               LISTEN      0          22985      4034/exim4          
tcp6       0      0 :::64295                :::*                    LISTEN      0          32486      6637/sshd: /usr/sbi 
tcp6       0      0 ::1:25                  :::*                    LISTEN      0          22986      4034/exim4          
tcp6       0      0 :::5355                 :::*                    LISTEN      997        13443      433/systemd-resolve 
udp        0      0 127.0.0.54:53           0.0.0.0:*                           997        13448      433/systemd-resolve 
udp        0      0 127.0.0.53:53           0.0.0.0:*                           997        13446      433/systemd-resolve 
udp        0      0 10.0.0.4:68             0.0.0.0:*                           998        12772      477/systemd-network 
udp        0      0 127.0.0.1:323           0.0.0.0:*                           0          13826      589/chronyd         
udp        0      0 0.0.0.0:5355            0.0.0.0:*                           997        13434      433/systemd-resolve 
udp6       0      0 ::1:323                 :::*                                0          13827      589/chronyd         
udp6       0      0 :::5355                 :::*                                997        13442      433/systemd-resolve 

### Done. Please reboot and re-connect via SSH on tcp/64295.


student@tpot-debian:~/tpotce$ sudo reboot

Broadcast message from root@tpot-debian on pts/1 (Tue 2024-09-17 23:10:21 UTC):

The system will reboot now!
