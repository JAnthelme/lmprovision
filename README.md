# Local Machine Provisionning
> With Ansible

## Installation

Install [Ansible](https://docs.ansible.com/ansible/2.3/intro_installation.html).

From the shell prompt (Ubuntu distros):
```sh
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```
Then
```sh
sudo ansible-pull setup.yml -U https://github.com/janthelme/lmprovision.git
```
The Vagrantfile is not necessary if you only run Ansible from GitHub repo, but can be used if running the script on a Vagrant vm.