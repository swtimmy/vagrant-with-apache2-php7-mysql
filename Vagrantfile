# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    #Ubuntu VM
	config.vm.box = "ubuntu/bionic64"
    config.vm.network "private_network", ip: "192.168.33.13"

    config.vm.provider "virtualbox" do |v|
        v.name = "Timmy-PHP-7.3"
        v.memory = 4096
    end

    # Mount the current directory for configuration
    #config.vm.synced_folder "./myproject", "/vagrant/myproject"
    config.vm.synced_folder "./myproject", "/vagrant/myproject", owner: "www-data", group: "www-data"

    config.vm.provision "ansible_local" do |ansible|
      ansible.compatibility_mode = "2.0"
      ansible.playbook = "ansible/master.yml"
      # ansible.sudo = true
    end

end
