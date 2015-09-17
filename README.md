meshmixer-vagrant
=================

A Vagrant configuration for running MeshMixer in a Lubuntu 14.04 virtual machine

[MeshMixer](http://www.meshmixer.com/) was experimentally [released for Ubuntu 
14.04 64bit](http://www.meshmixer.com/linux.html), but is currently broken on 
Ubuntu 15.04 (and, I assume, on many other distros). This Vagrantfile creates 
a minimal Lubuntu (LXDE) 14.04 virtual machine so you can run MeshMixer on 
your Linux distro of choice.

1. Install VirtualBox
2. Install Vagrant
3. Download the Vagrantfile from this repo
4. run `vagrant up`
5. Wait while it downloads and installs
6. Login to the GUI as user: vagrant, password: vagrant
7. Open a console
8. run `meshmixer`

