# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network :private_network, ip: "192.168.50.4"
  config.vm.synced_folder "vagrant/conf/", "/etc/apache2/sites-available/"
  config.vm.synced_folder ".", "/var/www/wordpress"
  config.vm.provision :shell, path: "vagrant/bootstrap.sh"
end
