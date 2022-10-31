# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "forwarded_port", guest: 3000, host: 3000, host_ip: "127.0.0.1"
  config.vm.network "forwarded_port", guest: 9090, host: 9090, host_ip: "127.0.0.1"
  config.vm.synced_folder "./files", "/vagrant_files", type: "rsync"
config.vm.provision "ansible" do |ansible|
  ansible.verbose = "v"
  ansible.playbook = "playbook.yml"
end
end