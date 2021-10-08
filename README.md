# Projet-Devops
# Prerequisites
- Vagrant
- VirtualBox

# Installation
1. Clone the repo and move in
2. Create yours VM with Vagrant
>  Vagrant up
3. Send ansible dir in "control"
>  vagrant upload ansible/ control
4. Connect on the "control" server
>  vagrant ssh "control"
5. In the ansible/ dir launch the playbook services
>  ansible-playbook playbook-install-services.yml -i inventory/default
You will probably have to launch it several times to get all in green
6. launch the playbook-install-wordpress.yml
> ansible-playbook playbook-install-wordpress.yml -i inventory/default
7. Add the hosts on your host machine
>  192.168.50.10 devsec.com
>  192.168.50.10 devops.com
>  192.168.50.10 devsecops.com
