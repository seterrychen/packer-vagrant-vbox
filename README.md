# packer-vagrant-vbox

Using Packer to package Vagrant box(driver: Virtualbox) by Docker. This is like [blacklabelops/hashicorp-virtualbox](https://github.com/blacklabelops/hashicorp-virtualbox) but using Ubuntu base image and only installing Packer, Vagrant and Virtualbox tools.

## Usage
* modprobe vbox modules on host by manual

        $ modprobe vboxdrv.ko
        $ modprobe vbox...
        $ docker run --rm -it --device /dev/vboxdrv:/dev/vboxdrv seterrychen/packer-vagrant-vbox

* Using privileged option to build vbox modules and modprobe modules from container

        $ docker run --rm -it --privileged=true --device /dev/vboxdrv:/dev/vboxdrv seterrychen/packer-vagrant-vbox
        root@container # apt-get update && apt-get install -y linux-headers-$(uname -r)
        root@container # /sbin/rcvboxdrv setup

## Tools info

* Packer = 0.10.0
* Vagrant = 1.8.1
* VirtualBox = 5.0.20  
