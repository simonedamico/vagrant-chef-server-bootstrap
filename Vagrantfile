# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.define "chef-server" do |chef_server|
    chef_server.vm.box = "precise64"
    chef_server.vm.host_name = "chefserver"
    chef_server.vm.network :hostonly, "10.253.0.10"

    config.vm.provision :chef_solo do |chef|
      chef.recipe_url = "http://s3.amazonaws.com/chef-solo/bootstrap-latest.tar.gz"
      chef.run_list.clear
      chef.json = {
        :chef_server=> {
          :url=> "http://localhost:4000",
          :webui_enabled=> true,
        }
      }

      chef.add_recipe "apt"
      chef.add_recipe "build-essential"
      chef.add_recipe "chef-server::rubygems-install"

    end
  end
end
