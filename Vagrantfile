# -*- mode: ruby -*-
# vi: set ft=ruby :
require 'socket'

host = Socket.gethostname.downcase

Vagrant.configure("2") do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.


  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.host_name = "your-name-for-example"
  config.vm.box = "precise64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"


  # Share code between your OS and vagrant, you can share as many folders as 
  # you want. How to share a folder:
  # config.vm.synced_folder("project-path-to-the-project-on-your-computer", "project-path-on-vagrant")
  # translated to:
  config.vm.synced_folder("/home/me/horizon", "/home/vagrant/horizon")

  config.vm.provider "virtualbox" do |v|
    # Allow symlinks
    v.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]

    # Use host DNS and routes
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]

    # Set VM memory
    v.customize ["modifyvm", :id, "--memory", 2048]
    v.customize ["modifyvm", :id, "--cpus", 2]
  end

end
