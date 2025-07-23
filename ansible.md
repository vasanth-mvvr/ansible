# ** ANSIBLE **
#Ansible is open sourced automation tool used for 
 * configuration management
 * Deployment management

# ** Configuration management **
Configuration management means we need to keep server ready before application deployment .
The server should ready with
* Installtion of packages
* Installation of builtin tools
* creation of systemctl services
* Installing runtime machies

# ** Ansible is popular for pull Vs push **
In oldern days when they were using chef,puppet etc they used to use
* Pull which means node needs to continuously chek for certain period in the configuration management weather there are any updates on it if yes it will pull and update.
* Push is popular because it is not like pull which goes and see the configuration management if there is any update in the configuration management it automatically pushes the upadates to all the nodes.

# ** Commands **
ansible installation of nginx -- manual 
```
ansible -i <ip address> -e ansible_user=<name> -e ansible_password=<password> -m dnf -a "name=<name of the module> state=<state of the module>" -b
``` 
NOTE::
* -i - inventory
* -e - enable
* -m - modules
* -a - arguments
* -b - become root user
ansible service for nginx -- manual 
```
ansible -i <ip address> -e ansible_user=<name> -e ansible_password=<password> -m service -a "name=<name of the module> state=<state of the module>" -b
``` 

ansible playbook
```
ansible-palybook -i inventory.ini -e ansible_user=<user> ansible_password=<password> 01_ansible.yaml
```
