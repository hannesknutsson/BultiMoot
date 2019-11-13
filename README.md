# BultiMoot
A collection of scripts and configurations for setting up a storage device for live booting and installing multiple different operating systems from ISO-files.


## Technical setup
The project is meant to be set up on a storage device set up in two partitions (or more if you want to use left over space for other stuff).

### Partition 1, FAT32
The first partition is meant to host configuration files for grub and the grub bootloader itself. This partition does not have to be large at all. My "grub partition" is currently 256MB, but could easily be much smaller.

The files meant to be in this partition are located in the directory "Partition1 FAT32" and can be directly copied onto your devices first partition.

### Partition 2, EXT4
This partition is used to store the ISO files we want to boot from. The ISO files should be located in the ISOFILES directory in the partitions root.

The partition should be of the type EXT4, or at least that is what I use and should therefore work for you too, but would probably work with other partition types too.

Operating system ISO files for booting from are pretty large (usually a gigabyte or two) and are therefore not hosted in this repository. These are very easily acquired online.

The ISO files should remain named as they are when acquired to work with as little effort as possible. If you really want, you can rename them, but then you will have to change the configuration files in the GRUB directory on partition 1 to work correctly.
