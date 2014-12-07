# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# Set the permissions on the vagrant key
FileUtils.chmod 0600, 'vagrant_private_key'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/trusty64"
    web.vm.network "private_network", ip: "192.168.25.101"
  end
  config.vm.define "queue" do |queue|
    queue.vm.box = "ubuntu/trusty64"
    queue.vm.network "private_network", ip: "192.168.25.102"
  end
  config.vm.define "database" do |database|
    database.vm.box = "ubuntu/trusty64"
    database.vm.network "private_network", ip: "192.168.25.103"
  end
end
