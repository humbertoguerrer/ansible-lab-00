# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end
  config.vm.define "meuservidor" do |meuservidor|
    meuservidor.vm.box = "ubuntu/focal64"
    meuservidor.vm.network "forwarded_port", guest: 80, host: 8080
    meuservidor.vm.network "public_network", ip: "192.168.15.7", bridge: "wlp5s0"
  end
end
