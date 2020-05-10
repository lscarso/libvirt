#Gnome Boxes
Set Gnome Boxes windows to 1440x900

#Set SELINUX Label
semanage fcontext -a -t svirt_image_t "/home/public/VMs(/.*)?"
restorecon -R /home/public

#Import VM
virsh create Windows-Virtual.xml

#VIRSH Configuration
EDITOR=nano virsh edit <your-vm-name>

Post OS installation:
#virtio drivers
https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/latest-virtio/virtio-win.iso
Install also Guest Agent (you can found it on the same iso)

#Spice guest tools
https://www.spice-space.org/download/windows/

#Spice Webdavd for folder share
https://www.spice-space.org/download/windows/spice-webdavd/

