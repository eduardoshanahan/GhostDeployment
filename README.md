# Running Ghost in Vagrant
I am trying this script in Ubuntu 13.04. For it I use Vagrant, hosting the machine under Virtualbox. If you don't have Virtualbox in your machine, click the link and follow the instructions. [get VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Having Virtualbox installed, fire the Vagrant instance doing
```
#!bash
cd GhostDeployment
vagrant up
```
To run the scripts I am using Python Fabric. If you don't have it, here is a script to deploy it in Ubuntu
```
#!bash
sudo ./install_fabric.sh
```
Having the tools in your host machine, make sure that all is in the right place:
```
#!bash
fab vagrant server_update
```
Now go with Ghost:
```
#!bash
fab vagrant install_tools
fab vagrant install_ghost
fab vagrant server_reboot
```
TODO: add the details to edit config.js and access Ghost from the host browser