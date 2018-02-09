# automate_deployment
This is a project for automating the deployment of a Ruby on Rails application using Ansible.
The playbooks can be tested with Vagrant using the provided Vagrantfile.

There are three main roles:
- common: the tasks in this playbook will create a user, configure ssh login and update the package manager cache.
- web: the tasks in this playbook will install Git, Ruby, Rails, MySQL and Apache.

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
