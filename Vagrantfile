# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.define "nginx2_server" do |nginx2|
    nginx2.vm.box = "debian/bullseye64" 
    nginx2.vm.hostname = "nginx2.sistema.test"  
    nginx2.vm.network "private_network", ip: "192.168.57.101"  
    nginx2.vm.provider "virtualbox" do |vb|
      vb.memory = "512"  
    end
    nginx2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx2
    SHELL
  end

  config.vm.define "nginx_server2" do |nginx2|
    nginx2.vm.box = "debian/bullseye64" 
    nginx2.vm.hostname = "nginx2.sistema.test"  
    nginx2.vm.network "private_network", ip: "192.168.57.102"  
    nginx2.vm.provider "virtualbox" do |vb|
      vb.memory = "512"  
    end
    nginx2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx
    SHELL
  end

end
