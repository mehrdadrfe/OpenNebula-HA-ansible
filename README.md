# OpenNebula-HA-ansible

Ansible playbooks to deploy Opennebula with high availability. 
This playbooks support deployment on *CentOS 7* .

This inventory includes some roles to configure yum repositories and install opennebula server with mariadb. 

Feel free to integrate this into your own way of doing things.

Currently these playbooks configure a basic Opennebula setup. Things like SSL, LDAP, Gluster etc.. are not yet included. 

## How to use

### Edit the Hosts
Edit the +hosts+ file. Put the nodes under +[one]+

```
[one]
192.168.10.31
192.168.10.32
```
### Execute the playbooks
Execute the +opennebula+ playbook to deploy all roles.

```
ansible-playbook -i hosts opennebula.yml -K
```


---

We assume you have checked variables in roles.
