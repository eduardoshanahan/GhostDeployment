# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "raring64"
  config.vm.box_url = "http://goo.gl/ceHWg"
  config.vm.network :forwarded_port, guest: 2368, host: 2368
  config.vm.provider :virtualbox do |vb|
    vb.name = "Ghost-Deployment"
  end
end
