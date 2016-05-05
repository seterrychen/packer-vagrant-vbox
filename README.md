# packer-vagrant-vbox

Using Packer to package Vagrant box(driver: Virtualbox) by Docker. This is like [blacklabelops/hashicorp-virtualbox](https://github.com/blacklabelops/hashicorp-virtualbox) but using Ubuntu base image and only installing Packer, Vagrant and Virtualbox tools.

## Using

        $ docker run --rm -it --privileged=true --device /dev/vboxdrv:/dev/vboxdrv seterrychen/packer-vagrant-vbox

## Tools info

* Packer = 0.10.0
* Vagrant = 1.8.1
* VirtualBox = 5.0.20  
