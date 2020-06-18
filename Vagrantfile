# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider :libvirt do |libvirt|
    libvirt.hyperv_feature :name => 'relaxed', :state => 'on'
    libvirt.hyperv_feature :name => 'vapic', :state => 'on'
    libvirt.memory = "1024"
    libvirt.volume_cache = "unsafe"
  end  # The most common configuration options are documented and commented below.
  # find more boxes: https://app.vagrantup.com/boxes/search

  config.vm.box = "peru/windows-server-2012_r2-standard-x64-eval"
  config.vm.box = "peru/windows-server-2016-standard-x64-eval"
  config.vm.box = "peru/windows-server-2019-datacenter-x64-eval"
  config.vm.box = "centos/8"
  config.vm.box = "generic/fedora32"
  config.vm.box = "generic/ubuntu2004"
  config.vm.box = "peru/ubuntu-20.04-desktop-amd64"


  config.vm.define "test" do | test |
    test.vm.hostname = "test"
    test.vm.network "private_network", ip: "192.168.33.10"
    #dc.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "dc-playbook.yml"
    #end
  end

end
