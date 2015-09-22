# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = 2048
    vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
  end

  config.vm.provision "shell", inline: <<-SHELL
    cd /home/vagrant
    sudo sh -c 'echo "deb http://s3.amazonaws.com/autodesk-meshmixer/meshmixer/ amd64/" > /etc/apt/sources.list.d/meshmixer.list'
    sudo apt-get update
    sudo apt-get dist-upgrade
    sudo apt-get install -y vim lubuntu-core notify-osd
    sudo apt-get install -y lubuntu-core
    sudo mkdir /home/vagrant/Documents
    sudo chown vagrant:vagrant /home/vagrant/Documents
    sudo apt-get install -y --force-yes meshmixer
    sudo shutdown -r now
  SHELL

end
