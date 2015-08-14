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

### Notes

This provisioning does not create a new Symfony2 project but only install the Symfony installer. It's up to you to create a new project (see Symfony2 installation doc) or clone your existing project in the sources folder (ignored by gitignore).

# Variables
* **database_name:** MySQL database used by project
* **nginx_project_root:** project root used by nginx
* **nginx_project_name:** project name used to write nginx log file

# Notes
## Run playbook locally

In case you are running this using Windows, you can play the playbook locally using the command:

`ansible-playbook -i "localhost," -c local playbook.yml`
