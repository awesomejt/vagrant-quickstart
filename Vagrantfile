# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "tomcat8"

  config.vm.network "forwarded_port", guest: 8080, host: 8080
  
  config.vm.provision "shell", path: "provision-tomcat.sh"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "TomcatDev"
    vb.memory = "1024"
    vb.cpus = 2
  end
end
