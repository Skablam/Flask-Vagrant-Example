# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "hashicorp/precise64"

  config.ssh.forward_agent = true
  config.vm.network "private_network", :ip => "172.16.42.43"
  config.vm.network "forwarded_port", guest: 5000, host: 5000
  config.vm.provision :shell, :path => 'script/provision'

end
