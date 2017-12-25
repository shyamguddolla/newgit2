# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.ssh.insert_key = false
config.vm.provider :virtualbox do |vb|
vb.customize ["modifyvm", :id, "--memory", "1024"]
 end

 # manager
 config.vm.define "JenkinsServer" do |app|
 app.vm.hostname = "JenkinsServer"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.61.11"
 end
 # control
 config.vm.define "QAServer" do |app|
 app.vm.hostname = "QAServer"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.61.22"
 end
 # control
 config.vm.define "ProdServer" do |app|
 app.vm.hostname = "ProdServer"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.61.13"
 end
 
 
 end
