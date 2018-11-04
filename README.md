# Local Machine Provisionning
> With Ansible (Ubuntu-based distros)

## Installation

Install [Ansible](https://docs.ansible.com/ansible/2.3/intro_installation.html) and git.

From the shell prompt:
```sh
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible git
```
Rename user0 (in `setup.yml`) to your user name, then run:
```sh
sudo ansible-pull setup.yml -U https://github.com/janthelme/lmprovision.git
```
If running from a cd-rom, remove (comment-out) the cd-rom from `/etc/apt/sources.list` file. E.g. with this script:
```sh
awk '$0="# "$0' /etc/apt/sources.list  > /etc/apt/sources.list.tmp && mv /etc/apt/sources.list.tmp /etc/apt/sources.list
```
The Vagrantfile is not necessary if you only run the Ansible playbook from GitHub repo, but can be used if running it on a Vagrant vm.
