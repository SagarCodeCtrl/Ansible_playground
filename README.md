# Automation with Ansiable
<p align="center">
<img alt="Ansible" width="270px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/ansible/ansible-original.svg" style="padding-right:10px;" /> 
</p>
</br>
<h3> <strong> Read the detailed article on: </strong> </h3> <a href = "https://medium.com/@sagarkrp/automation-with-ansible-101-27f709f4f8a" target ="_blank"> 
 
<picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://github.com/sagarkrp/sagarkrp/blob/main/images/Medium-white1x.png" width="160px" height="35px">
   <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sagarkrp/sagarkrp/main/images/Medium-dark.svg" width="160px" height="35px"> 
   <img alt="Medium Alternative Theme." src="https://raw.githubusercontent.com/sagarkrp/sagarkrp/main/images/Medium-dark.svg" width="160px" height="35px">
</picture> </a>

Introduction:
-------------
Ansible is an open source configuration management utility. It can automate and standardize the configuration of remote hosts and virtual machines. We can perform application installation, system update and many such operations.

Why use Ansible:
---------------
Ansible is very handy when it comes to installation of software on large numbers of machines. But why ansible when we can use Chef or Puppet.

- Ansible uses YAML scripts which is very easy to understand. (While others use Ruby and a specific DSL)
- Ansible is agent less. It uses SSH which is already present in all the machines. So we dont need to install ansible on all the destination machines. We install it on only one machine which we call Master Node. (Others need agents to be installed on the destination machines)
- Ansible is push based system, meaning whatever we specify on our script on the master node, and run command or execute a playbook, the controller node initiates the execution and pushes the necessary tasks and configurations to the managed nodes over SSH. Each managed node runs the tasks locally based on the received instructions.

<h1> Terminologies used in Ansible: </h1>

Playbooks:
----------
- Playbooks are written in YAML format and define the desired state of a system. It contains of a set of tasks and configurations that Ansible executes on target hosts. Playbooks provide a high-level abstraction and allow you to describe complex automation workflows.

Inventory: 
-----------
The inventory file in Ansible defines the hosts or managed nodes on which tasks are executed. It can be a static file listing hostnames or IP addresses, or a dynamic inventory script that fetches host information from external sources like cloud providers or databases.

Modules:
--------
Ansible provides a wide range of built-in modules that abstract common system operations such as package installation, file management, service management, user management, and more. Modules are used in playbooks to perform specific tasks on target hosts.
Tasks: Tasks are the individual steps within a playbook that Ansible executes sequentially. Each task maps to a module and defines the desired state or action to be performed on the target hosts.

Roles: 
------
Roles are a way to organize and encapsulate related tasks, handlers, and files into reusable units. They promote code reuse and allow for a modular approach to configuring systems. Roles can be shared and used across multiple playbooks.

Inventory Groups:
-------------
Ansible allows you to organize hosts into groups within the inventory file. Grouping hosts enables you to target specific subsets of hosts and apply different configurations or tasks based on their roles or characteristics.

Ansible Vault:
-----------
Ansible Vault provides encryption and decryption capabilities to protect sensitive data such as passwords, API keys, or certificates. It allows you to securely store and use confidential information within your playbooks.

Ansible Galaxy:
--------------
Ansible Galaxy is a platform for sharing and discovering Ansible roles and collections created by the community. It provides a vast collection of pre-written roles that can be easily integrated into your playbooks.
