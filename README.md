# yocto-raspberrypi0-conf
my config files and notes for building yocto for raspberry pi zero.

## Commands to build single package and add it to the board
### Host machine commands:
- `bitbake <package name>`
- `bitbake package-index`

### Fire up the the http server on the host:
- `cd tmp/deploy/rpm`
- `sudo python3 -m http.server --bind <Local IP> 80`

### Target machine commands:
- `dnf clean metadata`
- `dnf install <package name>`

## Build History:
- 1st - simple build for rpi0
- 2nd - hwup for rpi0
- 3rd - hwup for rpi0 with systemd
