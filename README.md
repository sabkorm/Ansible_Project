# Ansible project

## Overview
This Ansible project is separated into two parts, executing different tasks on the host machines.

### Ansible project I:

- Installing different packages on the host machines (htop, tree)
- Updating the system
- Installing Apache/httpd
- Copying files to host machines
- Printing onto the screen how many RedHat hosts are there, and how many Debian hosts are there

### Anible Project II:

- Copying files from the master machine onto the host machine
- Using a loop to print certain messages
- Printing on screen the OS family of the host machine
- Creating a text variable, and printing it

Using delegation:
- Saving the hosts' IPs into a log.txt file on the master
- Rebooting the hosts
- Saving the timestamp when the hosts rebooted into the log.txt

## Ansible components

### Ansible configuration file
The Ansible configuration file (`ansible.cfg`) contains the default configuration relevant to the roles' tasks that will be used in this project. For example, the path to the `hosts` file with the information of the host machines that will be used.

### Hosts file
The `hosts` file contains the host machines on which the Ansible tasks run on. It contains the host machines' names, their IP addresses, and the groups the hosts are sorted into.

### Variables
In the `group_vars` folder, we can specify variables that are relevant to the hosts by the groups we sorted them into. For example, the path to the folder in which the SSH public key to access them with can be found, or the username of the host machine.

### Roles
The `roles` folder contains the yml files that specify the tasks that would be executed using the host machines. In this project, the Role yml file points to the Role's folder with the same name, which cointains additional folders, such as the Tasks folder, which contains the yml file spacifying the tasks that the host machines will perform, the Files folder that contains the files relevant to the tasks, etc.