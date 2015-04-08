# Ansible-Webserver
Ansible provisioning configuration for webservers using nginx/php-fpm/mysql and Symfony2

## Components

* nginx
* php-fpm
* php-cli
* intl
* PDO
* mysql
* symfony installer
* phpmyadmin

## Configuration
### Ubuntu box

Ubuntu Server Trusty 14.04 from Vagrantbox.es

https://oss-binaries.phusionpassenger.com/vagrant/boxes/latest/ubuntu-12.04-amd64-vbox.box

### Virtual Machine

* NFS shared folders (sorry for Windows users... You should change your OS, really).
* DHCP private network
* Port bindings
  * 80 -> 8080 : web application
  * 8081 -> 8081 : phpmyadmin
* Provisioning from Ansible provisioner, so you have to install Ansible to your Vagrant host (see Vagrant doc for more information)

# Variables
* **database_name:** MySQL database used by project
* **nginx_project_root:** project root used by nginx
* **nginx_project_name:** project name used to write nginx log file
