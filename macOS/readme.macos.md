## Opencore
https://dortania.github.io/OpenCore-Desktop-Guide/


## Configure OpenCore
### How to mount a qcow2 disk image
#### Step 1 - Enable NBD on the Host
modprobe nbd max_part=8
#### Step 2 - Connect the QCOW2 as network block device
qemu-nbd --connect=/dev/nbd0 /home/public/VMs/macOS/OpenCore.qcow2
#### Step 3 - Find The Virtual Machine Partitions
fdisk /dev/nbd0 -l
#### Step 4 - Mount the partition from the VM
mount /dev/nbd0p1 /mnt/somepoint/
#### Step 5 - After you done, unmount and disconnect
umount /mnt/somepoint/
qemu-nbd --disconnect /dev/nbd0
rmmod nbd


#### Download OpenCore.qcow2 and config.plist
https://github.com/kholia/OSX-KVM

#### Change screen resolution on config.plist

<key>Resolution</key>
<string>1440x900@32</string>

#### Copy config.plist on OpenCore.qcow2

# Post configuration

## Store problem
### en0
cd /Library/Preferences/SystemConfiguration/
rm preferences.plist
rm NetworkInterfaces.plist

## Mouse
QemuUSBTablet-1.2 ???
