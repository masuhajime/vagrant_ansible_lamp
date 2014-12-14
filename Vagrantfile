# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65"
  # centos65はsshできる
  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"

  config.vm.network "private_network", ip: "192.168.33.10", :netmask => "255.255.255.0"

  config.vm.provider "virtualbox" do |v|
    v.gui = false
    v.memory = 1024
    v.name = "centos65lamp"
    v.customize ["modifyvm", :id, "--usb", "off", "--usbehci", "off"] # usb2.0 off
  end

  config.vm.provision "ansible" do |ansible|
    ansible.sudo = true
    ansible.playbook = "playbook.yml"
  end
end
