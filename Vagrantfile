# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.cache.scope = :box if Vagrant.has_plugin?("vagrant-cachier")

  config.vm.provider :virtualbox do |vb, override|
    vb.name = "sushi"
    vb.memory = 2048
    vb.cpus = 4
    vb.customize ["modifyvm", :id, "--chipset", "ich9"]

    override.vm.box = "ubuntu/trusty64"
  end
end
