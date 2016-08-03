# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "debian/jessie64"

    # Rename the hostname from "default" to "vagrant" to clarify the intention of host_vars/vagrant.yml
    config.vm.define "vagrant" do |vagrant|
        config.vm.hostname = "vagrant"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "site.yml"
    end
end
