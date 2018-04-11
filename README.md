# yocto-raspberrypi0-conf
my config files and notes for building yocto for raspberry pi zero.

Builds:
1st - simple build for rpi0
2nd - hwup for rpi0
3rd - hwup for rpi0 with systemd


Commands to build single package and add to board
Host machine:
bitbake <package name>
bitbake package index

# run the http server
cd tmp/deploy/rpm
sudo python3 -m http.server --bind 192.168.0.168 80

Target machine:
dnf clean metadata
dnf install <package name>
