# My-Ansible-Playbooks
Repository for my Ansible Playbooks:

1. AddingUserToGroup.yml

- Add a new user called usertest1 in the group users.
- Create its home directory.

2. CopyFileFromLocalToRemote.yml

- Playbook to copy from source (local) to dest(remote)

3. DeletingUsersFromGroup.yml

- Delete the user usertest2.
- Delete its home directory from the system.

4. PingForTestingPurposes.yml

- For test only. 
- It performs a ping on the host defined in /etc/ansible/hosts.

5. RemovingSpecificUsersFromGroup.yml

- Remove all users with name that start from user* from the group users.
- Will also remove all users except those who start with ext*, use "-g wheel" and "grep -v ext*".
- The playbook has been tested on Centos and Debian.

6. SNMPConigurationAndPackages.yml

- Install the SNMP package.
- Configure the snmpd.conf.
- Setup logrotate for snmp.
- Configure the /etc/sysconfig/snmpd file.
- Add new firewall rules.
- Reload the firewall.
- Reload the snmpd service.
- All files handled by Ansible will have a comment at the top mentioning "This file is managed by Ansible for references".
- It has been adapter for Centos7 only.

7. LVMManipulation.yml

- Create a VG and LV.
- Format the dist to ext4.
- Mount the disk on specific directory.

8. UpdateGLIBCandRestartNamedService.yml

- update the Glibc packages
- Restart the named service.

9. GatherInformationAboutOS.yml

- Retrieve versions of Kernel, Networker, Shinken, BladeLogic and VMtool.
- The output will be appended on a file in /tmp/rhelroot.

10. ReplicateUserDirectoryAndKeys.yml

- Create account for non-existant users.
- Add the users to wheel group and setup the permissions.
- creating the .ssh directory and setup the permission.
- Configure SELINUX on the .ssh directory.
- Write key to authorized_key file directly using the bullet proof approach.

11. ChangePassword.yml

- change password of a user.
- Always use the hash of the password in the password field.
- The goal is to update the /etc/shadow file on the remote machines.

