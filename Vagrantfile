# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'bento/ubuntu-16.04'

  config.vm.provider 'virtualbox' do |vb|
    vb.memory = '512'
  end

  config.vm.define 'web1' do |web|
    web.vm.network 'private_network', ip: '192.168.33.111'
  end

  config.vm.define 'web2' do |web|
    web.vm.network 'private_network', ip: '192.168.33.112'
  end

  config.vm.define 'db1' do |db|
    db.vm.network 'private_network', ip: '192.168.33.121'
  end

  config.vm.define 'db2' do |db|
    db.vm.network 'private_network', ip: '192.168.33.122'
  end
end
