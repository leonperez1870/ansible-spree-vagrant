# Spree Commerce with Ansible

The purpose of this project is to automate a new Spree Commerce rails app with some bells and whistles. Vagrant will start 3 servers labeled ```development``` ```production``` and ```dbserver```
ATM this is a work in progress as I am working on being as clean as possible.

## Prerequistes

- Vagrant

Set the ```VMs``` variable to the IP addresses you want

Run ```vagrant up``` to spin up those three servers

- VirtualBox
Go to VirtualBox Preferences > Network > Host-only Networks
Add a host only network with your preferred IPv4 and IPv4 Network Mask

ssh to each one using ```ssh vagrant@ip.address``` password being ```vagrant```

- Ansible

```ansible-playbook -i inventory ansible/playbook.yml```
Sit back and enjoy

## Base Box

[geerlingguy/ubuntu1604](https://atlas.hashicorp.com/geerlingguy/boxes/ubuntu1604/)

## Dev Tools

- curl
- git
- vim
- htop
- mysql-client
- libmysqlclient-dev
- build-essential
- python-software-properties

## TODO

- Prepare MySQL DB
- Get Ruby
- Install Gems
- Set Rails
- Have rails server run its appropriate server
- Connect MySQL server
- Automate Git Flow
- GCE deployment
