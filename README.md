### Install

- Install Virtual Box - https://www.virtualbox.org/wiki/Downloads, the platform 
package and the extension pack
- Install Vagrant - http://www.vagrantup.com/downloads.html

### Configure
 
 - Create a folder where you want to keep the Vagrant box and projects. 

 ! All Vagrant commands have to be written inside the directory which has the
 Vagrantfile.

 - Copy the Vagrantfile provided - you can customize it. More about this:
 http://docs.vagrantup.com/v2/getting-started/index.html

 ! If you want another box type (default is precise64 which is Ubuntu on 64 bit),
 you can browse through them here https://www.vagrantcloud.com/, and update the
 Vagrantfile.

 - Clone your projects inside the directory, and update the Vagrantfile to
 share the folders. You should clone DevStack and the project you are interestd
 in at least. :)

 - Run `vagrant up` - the first time it will take longer, since it will add
 the box and download a lot of stuff

 ### Setup

 - Login `vagrant ssh` and update your box. For Ubuntu you should do this:
    - $ sudo apt-get update
    - $ sudo apt-get upgrade
    - $ sudo apt-get autoremove

- Run the DevStack script - wait for a while, and then continue with your
project configuration.


### Other info

- To close a session just type `exit` or CTRL + D
- To close your box (like shutdown for computers) type `vagrant halt`
- To start the box type `vagrant up`. The box will have the same setup as it did
before you shut it down.


Happy coding! :)
