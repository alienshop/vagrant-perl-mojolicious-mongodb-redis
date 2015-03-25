# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/ubuntu-14.04"
  config.vm.box_url = "https://atlas.hashicorp.com/chef/boxes/ubuntu-14.04/versions/1.0.0/providers/virtualbox.box"
  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :forwarded_port, guest: 8080, host: 8080
  config.vm.network :forwarded_port, guest: 27017, host: 27017
  config.vm.network :forwarded_port, guest: 6379, host: 6379
  config.vm.provision "shell", path: "provision.sh"
end
