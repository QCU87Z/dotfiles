# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "generic/fedora31"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.name='my_vagrant_box'  
    vb.memory = 1024
  end
  # config.vm.provision :shell, inline: "dnf install ansible -y"
  
  # It would appear this is run from the local box. i.e. no windows
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "test.yml"
  end

end
