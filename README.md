# lab_ansible_playbook
Ansible Playbook for Zabbix Agent and Remote Share Mount
This Ansible playbook installs the Zabbix agent on remote hosts, and configures it to monitor a Windows share using CIFS mount. It also creates a new user with root access, and sets up the sudo group. To run the playbook, edit the secrets.yml file with the required information, and execute the playbook using the command ansible-playbook labs.yml.

Requirements
Ansible 2.9+
Access to remote hosts via SSH
Variables
zabbix_server_ip: IP address of the Zabbix server
asv_labs_password: Password for the new user
share_username: Username for the Windows share
share_password: Password for the Windows share
Playbook Tasks
Create sudo group
Create new user with root access and set password
Set zabbix conf file path
Install and enable Zabbix agent service
Set Zabbix agent IP and configure monitoring of BesClient
Create mount point directory and mount remote share
Note
Please make sure to edit the secrets.yml file with the required information before executing the playbook.
The mount remote share task in the playbook is currently disabled. If you need to mount a remote share, please modify the task with the appropriate parameters and ensure that the share is accessible from the target system.


