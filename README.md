vagrant-chef-server-bootstrap
=============================

Vagrant configuration for bootstrapping a chef server virtual machine

# Overview
I assume you already have an ubuntu 12.04 64 bit virtual machine. 

If you don't have one:
```vagrant box add precise64 http://files.vagrantup.com/precise64.box``` 

The new machine will be available at 10.253.0.10, please modify if it collide
with your existing networks. 

I used the latest opscode cookbooks for the boostrapping. 

The webui is available at http://10.253.0.10:4040 and should show you the default 
password for the admin user. 
