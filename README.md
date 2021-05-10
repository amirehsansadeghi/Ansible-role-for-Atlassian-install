Ansible role for Atlassian setup
=======================
ansible Version 2.8.x

### ATTENTION: DO NOT TEST THIS SCRIPTS, IT'S ONLY COMMITED FOR ARCHITECTURE REVIEW AND IT STILL NEEDS CHANGES TO BE FUNCTIONAL ###

### NOTE: database username and passwords are defined in variable file (inventories-->dev-->group_vars-->all-->mysql_users), please replace it with suitable USERNAME and PASSWORD for your personal use

## Role based Install (prepare, delete, install and etc.)
```
## playbook for add users and groups to hosts
ansible-playbook -i inventories/dev/group_vars/all  plays/add-user-group.yml --user=root

## playbook for install software dependencies to hosts
ansible-playbook -i inventories/dev/group_vars/all  plays/prepare.yml --user=root

## playbook for install the whole package together
ansible-playbook -i inventories/dev/group_vars/all  plays/install.yml --user=root

# playbook for delete everything that installed before
ansible-playbook -i inventories/dev/group_vars/all  plays/delete.yml --user=root




