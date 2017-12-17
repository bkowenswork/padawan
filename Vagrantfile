# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "jenkins-server"
    config.vm.box_url = "~/vagrant/ubuntu-14.04-amd64.box"
    config.vm.hostname = "jenkins-server"
    config.vm.network :private_network, ip: "10.0.15.50"
    config.vm.network "forwarded_port", guest: 80, host: 8090
    config.vm.network "forwarded_port", guest: 443, host: 9443  
    config.vm.provision "shell" do |s|
        s.path = "provision.sh"
    end
end
