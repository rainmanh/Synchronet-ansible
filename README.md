# Synchronet-ansible
Synchronet BBS -- Deployment Automation written in Ansible with Vagrant Support

This is a POC for the Deployment of Synchronet  BBS using the following technologies:

 * Ansible
 * Vagrant

It has been initially written for Ubuntu 16.04 but it should be for any Debian build.

How this work is like any other ansible playbook so example below(note parameters might be different up to your environment):

```
ansible-playbook main.yml -i hosts --user=<user> --extra-vars "ansible_ssh_pass=<passwd>" -vv
```

Or if SSH keys in the remote system:

```
ansible-playbook main.yml -i hosts --user=<user> -vv
```

You need to workout your own host settings based in your infrastructure. That would be at the **inventory** directory.

##Vagrant

if you are Using **Vagrant** :

```
vagrant up
```
Should create the test environment locally and you should be able of testing  your newly created BBS as follows:

```
telnet 192.168.33.2 23
```
Also note: you need to double check the Vagrantfile got the right port forwarding and IPs which might satisfy your environment.



## Versions Currently Supported through this Playbook

 * Ubuntu 16.04. Directory: Vagrant/ubuntu

 * Centos 7.x Directory: Vagrant/centos


## URL and Information

Synchronet BBS has been created by **Rob Swindell (a.k.a. Digital Man)**. (BBS software still fully supported ).

 * https://en.wikipedia.org/wiki/Synchronet
 * http://www.synchro.net/

 I can me reached at the following Fidonet addresses:

  * Gonzalo Fernandez Ordas@2:250/1.2
  * Gonzalo Fernandez Ordas@2:341/66.86

 Also my BBS: Unicyber BBS, can be reached as follows (free registration required):
  * telnet: bbs.unicyber.co.uk port: 2323
  * ssh: bbs.unicyber.co.uk port: 2424


  ## TO-DO

   - Ubuntu 18.04 (testing)
   - Templates
   - iptables
