unpack
Boot = boot.img
unmkbootimg version 1.2 - Mikael Q Kuisma <kuisma@ping.se>
Kernel size 5677280
Kernel address 0x80208000
Ramdisk size 357803
Ramdisk address 0x81800000
Secondary size 0
Secondary address 0x81100000
Kernel tags address 0x80200100
Flash page size 2048
Board name is ""
Command line "console=ttyHSL0,115200,n8 androidboot.hardware=mako lpj=67677"

*** WARNING ****
This image is built using NON-standard mkbootimg!
OFF_RAMDISK_ADDR is 0x01600000
Please modify mkbootimg.c using the above values to build your image.
****************

Extracting kernel to file zImage ...
Extracting root filesystem to file initramfs.cpio.gz ...
All done.
---------------
To recompile this image, use:
  mkbootimg --kernel zImage --ramdisk initramfs.cpio.gz --base 0x80200000 --cmdline 'console=ttyHSL0,115200,n8 androidboot.hardware=mako lpj=67677' -o new_boot.img
---------------
1202 blocks

mkbootimg --kernel zImage --ramdisk initramfs.cpio.gz --base 0x80200000 --cmdline 'console=ttyHSL0,115200,n8 androidboot.hardware=mako lpj=67677' -o new_boot.img

boot_info  ../boot.img 
boot_info  new_boot.img 

fastboot flash boot new_boot.img 
