# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"


  config.vm.network "forwarded_port", guest: 80, host: 8888

 
  config.vm.provision "shell", inline: <<-SHELL
    yum install -y epel-release
    yum install -y nginx
    systemctl start nginx
    systemctl enable nginx
  SHELL
end
