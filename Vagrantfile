# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  # Base box
  config.vm.box = "ubuntu/trusty64"

  # Configure port forwarding
  config.vm.hostname="vagrant-dev-vm"
  config.vm.network :forwarded_port, guest: 80, host: 4567, auto_correct: true
  config.vm.network :forwarded_port, guest: 8080, host: 8888, auto_correct: true

  # SSH username/password
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"

  # Provisioning
  config.vm.provision "shell", path: "bootstrap.sh"



end
