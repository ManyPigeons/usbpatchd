# usbpatchd

Patch the USB restriction on iOS 13, which blocks USB accessories from accessing the device.
This can be used to provide SSH over USB (courtesy of dropbear) from a locked
iOS device.

This is a free alternative to "minaUSB patcher" that is open-source and safer. Additionally, this works on checkm8-compatible devices that don't have a diagnostic menu to enter after boot unlike minaUSB.

Most files in this repository have been aligned similar to the checkra1n bootstrap
(/binpack); as such, the GPLv3 license applies as labelled in the [License section](#license)
to only the files that nick-botticelli has written (and therefore claims copyright on).

## Installation
Just clone the repository using git and cd into the directory:

`git clone https://github.com/ManyPigeons/usbpatchd.git && cd usbpatchd`

Update using:

`cd usbpatchd && git pull`

## Usage
1. Boot into an SSH ramdisk capable of SSH and mounting the System volume
    * A ramdisk capable of such can be created through a free public tool
    created by Nathan (verygenericname) which can be found
    [here](https://github.com/verygenericname/SSHRD_Script)

2. Run `install-usbpatchd.sh` from a new Terminal and follow any instructions.

## Notes
* The implementation itself is one 
nick-botticelli created for personal use but has found it to work 
perfectly for their needs (i.e. tested on A10 iOS 13 via macOS 12).

## TODO
* Fix iOS <= 12 support
* Rewrite installer in python

## License
`install-usbpatchd.sh`, `root/Library/LaunchDaemons/com.apple.usbpatchd.plist`,
and `root/usr/libexec/usbpatchd.sh` are copyright of Nick Botticelli and are licensed with the
[GNU General Public License Version 3](./LICENSE)
