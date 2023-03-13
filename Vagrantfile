# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 2
  end

  config.vm.define "nfss" do |srv|
    srv.vm.network "private_network", ip: "192.168.50.10"
    srv.vm.hostname = "nfss"
    srv.vm.provision "shell", path: "nfss_script.sh"
  end

end
