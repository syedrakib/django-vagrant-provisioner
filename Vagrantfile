# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.box_check_update = false
  config.vm.hostname = "django-helloworld"

  config.vm.network "forwarded_port", guest: 8000, host: 8001
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  config.ssh.forward_agent = true
  config.vm.synced_folder "./sourcecodes", "/home/vagrant/sourcecodes"
  config.vm.provider "virtualbox" do |vb|
    # # Don't boot with headless mode
    # vb.gui = true
    # Use VBoxManage to customize the VM. For example to change memory:
    vb.customize ["modifyvm", :id, "--memory", "1024"]
    vb.name = "django-helloWorld"
  end
  config.vm.provision "shell", path: "./vg-provisioner"
  config.vm.provision "shell", path: "./vg-provisioner-always", run: "always"
end
