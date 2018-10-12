# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.vm.define "vm1" do |node|
		node.vm.box        = "centos/7"

		node.vm.synced_folder "data/", "/mnt/data", create:true
		node.vm.network :private_network, :ip => "172.28.128.101"
		node.vm.provision :hosts, :sync_hosts => true
	end
	config.vm.define "vm2" do |node|
		node.vm.box        = "centos/7"

		node.vm.synced_folder "data/", "/mnt/data", create:true
		node.vm.network :private_network, :ip => "172.28.128.102"
		node.vm.provision :hosts, :sync_hosts => true
	end
end
