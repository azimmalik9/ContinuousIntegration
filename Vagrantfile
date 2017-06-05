# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  config.vm.hostname = "AZIM.qac.local"
  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "chad-thompson/ubuntu-trusty64-gui"
  config.vm.network :public_network, ip: "192.168.1.203"

  #Provisioning Script to install and configure system tools
  config.vm.provision :shell, path: "bootstrap.sh"

  #Setting up virtual box information, ram allocation, etc.
  config.vm.provider :virtualbox do |master|
  	master.gui = true
	master.name = "Azim Server"
	master.memory = 4096
	master.cpus = 2
   end  
   # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
   config.vm.synced_folder "shared", "/opt"
end




