# -*- mode: ruby -*-
# vi: set ft=ruby :

# Necesary PLUGINS:
# $ vagrant plugin install vagrant-junos

# To fix this error Message: LoadError: cannot load such file — vagrant-host-shell
# $ vagrant plugin install vagrant-host-shell

Vagrant.configure(2) do |config|
 
  config.vm.box = "juniper/ffp-12.1X47-D15.4"

  config.vm.define "vsrx01" do |vsrx01|
    vsrx01.vm.host_name = "vsrx01"
    vsrx01.vm.network "private_network",
                      ip: "192.168.10.1",
                      virtualbox__intnet: "LAN_1"
    vsrx01.vm.network "private_network",
                      ip: "192.168.20.1",
                      virtualbox__intnet: "LAN_2"
  end

  config.vm.define "vsrx02" do |vsrx02|
    vsrx02.vm.host_name = "vsrx02"
    vsrx02.vm.network "private_network",
                      ip: "192.168.10.2",
                      virtualbox__intnet: "LAN_1"
    vsrx02.vm.network "private_network",
                      ip: "192.168.20.2",
                      virtualbox__intnet: "LAN_2"
  end 

  # VirtualBox Configuration:

  config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  # vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
   vb.memory = "1024"
  end
  
 
end
