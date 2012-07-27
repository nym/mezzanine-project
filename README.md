# mezzanine-project


Create a mezzanine instance that runs inside a vagrant VM. 

## Install the prequisites

 * [Vagrant](http://vagrantup.com)
 * [Fabric](http://docs.fabfile.org)

 You can install fabric using pip.

## Download an Ubuntu VM image

    vagrant box add precise64 http://files.vagrantup.com/precise64.box

##  Run the Ubuntu VM image

    git clone http://github.com/lorin/mezzanine-project
    vagrant up
    fab all

## Access your mezzanine instance

Point your browser to <http://192.168.124.12>.

