# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.network "private_network", ip: "192.168.33.61"


   config.vm.synced_folder "./", "/vagrant", owner: "www-data", group: "www-data"

   config.vm.provider "virtualbox" do |vb|
     vb.memory = 4096
   end

   config.vm.provision "shell", inline: <<-SHELL
    add-apt-repository -y ppa:ondrej/php
    apt-get update
    apt-get -y upgrade

    apt-get install -y apache2
    if ! [ -L /var/www/html ]; then
      rm -rf /var/www/html
      ln -fs /vagrant /var/www/html 
    fi


    apt-get install -y php7.1 php7.1-common
    apt-get install -y php7.1-curl php7.1-xml php7.1-zip php7.1-gd php7.1-mysql php7.1-mbstring

    debconf-set-selections <<< 'mysql-server mysql-server/root_password password root'
    debconf-set-selections <<< 'mysql-server mysql-server/root_password_again password root'
    apt-get install -y mysql-server
    apt-get install -y php-mysql

    apt-get install -y libapache2-mod-php
    apt-get install -y composer
   SHELL
end
