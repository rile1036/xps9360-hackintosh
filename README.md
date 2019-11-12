# XPS 9360 Hackintosh Mojave

## Hardware

- Model : XPS 9360
- CPU : i7-7560u
- SSD : Toshiba thnsn5512gpuk 512GB
- Ram : 16GB
- DP : QHD+ 터치스크린
- Wifi : DW18930

## Certification Problem

Currently, mojave 14.6 requires a change of date.

This is because the Mojave version 14.6 certification period has expired.

Please change the date before September 30, 19.


## 4K Panic Problem

Use DVMT.efi from the DVMT directory.

0x785 to pre-assign DVMT, and enter the first command setup_var 0x785 to ensure that there is no return value.

The unmodified value is 0x01 (32M).

If no return value exists, do not continue to try the following.

This method is dangerous.

### grub> setup_var 0x4de 0x00
### grub> setup_var 0x785 0x06
### grub> setup_var 0x786 0x03