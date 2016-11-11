# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "bmcgonigle/centos68"

  config.vm.define "ldap" do |ldap|
          ldap.vm.network "public_network", ip: "192.168.50.15", bridge: "eth0"
	  ldap.vm.hostname = "ldap.og.com"
	  ldap.vm.network "forwarded_port", guest: 80, host: 8389

	  ldap.vm.provision "shell", 
   	    path: "ldap.provision.sh"
  end

end
