# Apache-Ansible
Configuration of Apache Server through DevOps Automation tool Ansible with yaml file and cmd line execution.

# Install Ansible on master system

$ wget ftp://mirror.switch.ch/pool/4/mirror/centos/7.3.1611/virt/x86_64/ovirt-3.5/common/ansible-2.3.1.0-1.el7.noarch.rpm

$ yum  localinstall ansible-2.3.1.0-1.el7.noarch.rpm

# Update Inventory

$ vim /etc/ansible/hosts

[web]

192.168.1.12  ansible_ssh_user=root  ansible_ssh_pass=redhat 

192.168.1.18  ansible_ssh_user=abcd  ansible_ssh_pass=redhat

# Run yml file

$ ansible-playbook --syntax-check  webserver.yml

$ ansible-playbook webserver.yml
