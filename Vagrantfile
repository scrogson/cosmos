# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

   config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y build-essential
      sudo apt-get install -y git
      sudo apt-get install -y vim
      sudo apt-get install -y nasm
      sudo apt-get install -y xorriso
      sudo apt-get install -y qemu
      curl -sSf https://static.rust-lang.org/rustup.sh | sh -s -- --channel=beta
  SHELL

  config.ssh.forward_x11 = true
end
