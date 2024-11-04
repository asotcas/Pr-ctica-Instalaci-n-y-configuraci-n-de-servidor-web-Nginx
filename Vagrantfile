# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.define "nginx_server" do |nginx|
    nginx.vm.box = "debian/bullseye64" 
    nginx.vm.hostname = "nginx.sistema.test"  
    nginx.vm.network "private_network", ip: "192.168.57.101"  
    nginx.vm.provider "virtualbox" do |vb|
      vb.memory = "512"  
    end
    nginx.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx
    SHELL
  end

end
