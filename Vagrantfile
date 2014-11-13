# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.package.name = "Ansible Remote Syslog VM"

  config.vm.box = "trusty"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.hostname = "remote-syslog.local"

  config.vm.network :private_network, ip: "10.0.0.14"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1048"]
    vb.customize ["modifyvm", :id, "--cpus", 2]
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "role.yml"
    ansible.inventory_path = "vagrant"
    ansible.limit = 'all'
  end
end
