# My-Ansible-Playbooks
Repository for my Ansible Playbooks:

1. AddingUserToGroup.yml

This playbook will Add a new user called usertest1 in the group users and will create its home directory as well.

2. CopyFileFromLocalToRemote.yml

Playbook to copy from source (local) to dest(remote)

3. DeletingUsersFromGroup.yml

This plabook will delete the user usertest2 and delete its home directory from the system

4. PingForTestingPurposes.yml

This playbook is for test only. It performs a ping on the host defined in /etc/ansible/hosts.

5. RemovingSpecificUsersFromGroup_CENTOS.yml

This playbook is removing all users with name that start from user* from the group users.
To remove all users except those who start with ext*, use "-g wheel" and "grep -v ext*".
Example: for i in $(lid -g users | grep -v ext* | cut -d '(' -f 1); do gpasswd -d $i wheel ; done

6. SNMPConigurationAndPackages.yml

This playbook will: 
- Install the SNMP package 
- Configure the snmpd.conf 
- Setup logrotate for snmp 
- Configure the /etc/sysconfig/snmpd file 
- Add new firewall rules
- Reload the firewall
- Reload the snmpd service.
- All files handled by Ansible will have a comment at the top mentioning "This file is managed by Ansible for references"
- It has been adapter for Centos7 only
