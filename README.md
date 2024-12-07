# Hey! I'm Filing Here

In this lab, I successfully implemented the following EXT2 file system, with a root directory, lost+found directory, hello world file, and a hello sym link.

## Building

To compile, run make. 

## Running

First, mount the directory:
mkdir mnt

Then, run the following set of commands to create the cs111-base image, mount the file system, and change the directory to mount. 
./ext2-create
sudo mount -o loop cs111-base.img mnt
cd mnt

Run ls -ain to view files, directories, symlinks, and their permissions. To dump filesytem information, run dumpe2fs cs111-base.img. To check the filesystem has been setup correctly, run  fsck.ext2 cs111-base.img.

## Cleaning up

Change out of the mount directory, unmount the file system, remove the directory, and clean up the executables using the following set of commands:

cd .. 
sudo umount mnt 
rmdir mnt 
make clean 