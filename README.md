# mezzanine-project

Do a production-style deployment of mezzanine inside an Ubuntu virtual machine (VM).

The deployment uses Fabric scripts that come with Mezzanine. It configures PostgreSQL as the backend database, gunicorn as the WSGI server, Nginx as the front-web server with memcached, and Supervisor to control gunicorn.

## 1. Install the prequisites

 * [Vagrant](http://vagrantup.com) for managing VirtualBox-based virtual machines.
 * [Fabric](http://docs.fabfile.org) for automating the installation of Mezzanine.

 You can install fabric using pip.

## 2. Download an Ubuntu VM image

Run the following command once to import an Ubuntu 12.04 ("Precise Pangolin") image.

    vagrant box add precise64 http://files.vagrantup.com/precise64.box

## 3. Download this repository

If you haven't downloaded this repository yet, grab it from github:

    git clone http://github.com/nimbis/mezzanine-project

##  4. Boot the virtual machine and install Mezzanine

Use Vagrant to boot the virtual machine and Fabric to install Mezzanine.

    cd mezzanine-project
    vagrant up
    fab all


## Access Mezzanine

Point your browser to <http://192.168.124.12>.

Log in to the admin interface <http://192.168.124.12/admin/> using the default account (username: `admin`, password: `default`).

You can also ssh to access the virtual machine (username: `vagrant`, password: `vagrant`).


## Tear down your virtual machine

When you're all done, bring down your virtual machine.

    vagrant destroy