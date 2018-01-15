# automate_deployment
This is a project for automating the deployment of a Ruby on Rails application using Ansible.
The playbooks can be tested with Vagrant using the provided Vagrantfile.

There are three main roles:
- common: the tasks in this playbook will create a user and set the server up for ssh login using ssh keys.
- db: the tasks in this playbook will install the MySQL database and change the root user account's password.
- web: the tasks in this playbook will install Git, Ruby, Rails and Apache while also adding a MySQL user for the application.

To run this project, Virtualbox, Vagrant and Ansible need to be installed:
```
$ sudo apt install virtualbox vagrant ansible
```
Afterwards, install the virtualbox guest additions plugin for Vagrant:
```
$ vagrant plugin install vagrant-vbguest
```
Finally, You can start the Vagrant virtual machine using the command:
```
$ vagrant up
```
The previous command will automatically execute the Ansible playbooks after creating the virtual machine.

In case the Ansible playbooks need to be executed again after changes:
```
$ vagrant provision
```
Finally, to stop the Vagrant machine:
```
$ vagrant destroy
```
