# Synchronet-ansible
Synchronet BBS -- Deployment Automation written in Ansible with Vagrant Support

This is a POC for the Deployment of Synchronet  BBS using the following technologies:

 * Ansible
 * Vagrant

It has been initially written for Ubuntu 16.04 but it should be for any debian build.

How this work is like any other ansible playbook so example belows(note parameters might be different up to your environment):

```
ansible-playbook main.yml -i hosts --user=<user> --extra-vars "ansible_ssh_pass=<passwd>" -vv
```

Or if SSH keys in the remote system:

```
ansible-playbook main.yml -i hosts --user=<user> -vv
```

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

 * Ubuntu 16.04
 * Centos 7.x


##TO-DO

 - Ubuntu 18.04 (testing)
 - Templates
 - iptables
