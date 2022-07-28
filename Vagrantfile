# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.box_check_update = true
  config.vm.boot_timeout = 600

  config.vm.provider "virtualbox" do |virtualbox|
    virtualbox.name = "devops-cd-vagrant-experiment"
    virtualbox.gui = false
  end

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.56.2"
  config.vm.synced_folder "./data", "/host_data"

  config.vm.provision "shell", inline: <<-SHELL
    apt update
    apt install -y nginx
  SHELL
end
