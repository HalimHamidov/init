service ssh status
apt-get install apache2
df
top
ps
kill
ifconfig
ping
netstat
route
traceroute
hosts
networks
host.conf
resolve.conf
interfaces

https://en.wikipedia.org/wiki/Resolv.conf
https://ru.wikipedia.org/wiki/DNS
[Настольная книга по Linux](https://ru.wikibooks.org/wiki/%D0%9D%D0%B0%D1%81%D1%82%D0%BE%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D0%BA%D0%BD%D0%B8%D0%B3%D0%B0_%D0%BF%D0%BE_Linux)
https://en.wikibooks.org/wiki/AWK
https://en.wikipedia.org/wiki/AWK


https://ru.wikipedia.org/wiki/Ifconfig
https://www.freebsd.org/cgi/man.cgi?query=ifconfig&sektion=8
https://www.manpagez.com/man/8/ipconfig/
https://ru.wikipedia.org/wiki/ARP

https://www.youtube.com/watch?v=cn8Zxh9bPio

https://github.com/VBrazhnik/init/wiki/Network
https://github.com/agavrel/42-Init
https://github.com/acuD1/init



ssh apearl@192.168.56.101
scp hello apearl@192.168.56.2:hello

/*https://wiki.enchtex.info/tools/console/scp*/

il-c2% ssh apearl@192.168.56.2

#google проброс портов для ssh подключения virtualbo

The authenticity of host '192.168.56.2 (192.168.56.2)' can't be established.
ECDSA key fingerprint is SHA256:Yp8RkDhIvcRIw52WReeRr4kJCdNMd5hLr3SCrOB5abM.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '192.168.56.2' (ECDSA) to the list of known hosts.
apearl@192.168.56.2's password:
Linux debian10 4.19.0-6-amd64 #1 SMP Debian 4.19.67-2+deb10u1 (2019-09-20) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Mon Nov 11 22:13:54 2019 from 127.0.0.1


*****************************************
sudo vim /etc/network/interfaces in apearl@debian10
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

allow-hotplug enp0s3
auto enp0s3
iface enp0s3 inet static
address 10.0.2.1
gateway 10.0.2.2
netmask 255.255.255.252

allow-hotplug enp0s8
auto enp0s8
iface enp0s8 inet static
address 192.168.56.2
netmask 255.255.255.252
..


