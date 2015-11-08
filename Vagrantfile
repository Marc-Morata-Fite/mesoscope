# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 5050, host:5050
  config.vm.network "forwarded_port", guest: 8080, host:8080


  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  config.vm.provider "vmware_fusion" do |vmw|
    vmw.vmx["memsize"] = "2048"
  end

  config.vm.provision "shell", path: "vagrant/install.sh"
end
