# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos"

  config.vm.define :snmp do |h|
    h.vm.network "private_network", ip: "10.1.1.2"
  end

  config.vm.define :prometheus do |h|
    h.vm.network "private_network", ip: "10.1.1.3"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "site.yml"
  end

end
