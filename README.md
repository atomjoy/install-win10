# Install Windows 10 from Linux
How to create Windows bootable usb from linux Debian 13.

## Windows bootable usb

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
7. Create sources directory on fat32 partition and copy /sources/boot.win from iso files to this directory
8. Remove usb safely. Thats all.
```


## Debian bootable usb (only linux iso)

```sh
# Add path if fdisk missing on Debian 13
PATH="/sbin:$PATH"

# Check usb device name
df or fdisk -l

# Copy iso
sudo dd if=debian-13.iso of=/dev/sdb bs=4M status=progress oflag=sync
```
