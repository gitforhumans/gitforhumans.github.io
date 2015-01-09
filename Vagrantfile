# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "precise64_vmware"

  config.vm.provider "vmware_fusion" do |vb|
    vb.gui = false
    vb.memory = "512"
  end

  # config.vm.provision "file", source: "vm/id_rsa", destination: ".ssh/id_rsa"
  # config.vm.provision "file", source: "vm/id_rsa.pub", destination: ".ssh/id_rsa.pub"
  # config.vm.provision "file", source: "vm/.gitconfig", destination: ".gitconfig"

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline <<-SHELL
    sudo apt-get -y install git apache2
  SHELL
end
