# h3c-inode
h3c inode 802.1x

cd src
ls
autoupdate
ls -la
autoreconf
automake --add-missing
ls
vi configure.ac
automake --add-missing
ls
./configure
make
vi md5-buildin/md5_dgst.c
make

root@armbian:/lib/systemd/system# cat njit.service
[Unit]
Description=njit H3C inode process
After=network-online.target syslog.target nfw.target
Wants=network-online.target

[Service]
Type=simple
ExecStartPre=
ExecStart=/usr/sbin/client user password  eth0
Restart=always
RestartSec=5

[Install]
WantedBy=multi-user.target
Alias=
