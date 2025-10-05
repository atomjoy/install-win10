# Install Windows 10 from Linux
How to create Windows bootable usb from linux Debian 13.

## Run

Download Windows10 ISO

```sh
1. Run gparted select your usb
2. Create new device (msdos) MBR not GPT
3. Create 2 partitions
  - 2GB fat32
  - 10GB NTFS
4. Mount iso (click 2 times)
5. Copy all files from iso to NTFS partition 
6. Copy all files from iso without sources to fat32 partition
7. Create sources directory in fat32 partition and copy /sources/boot.win from iso files to this directory
8. Remove usb safely. Thats all.
```

