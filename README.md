# Ubuntu 14.04LTS docker deployment with multi node consul and registrator

Both consul and registrator are deployed without using host networking.
All nodes get iptable rules applied to allow unlimited traffic between the nodes and incoming SSH.

## Prerequisites

- Ansible
- Vagrant

## Running it

All commands should be run from inside this folder, unless stated explicitly

Start up the environment (composed of 4 vagrant boxes):

```
vagrant up
```

To apply the ansible playbook:

```
# Install angstwad.docker_ubuntu role first:
ansible-galaxy install angstwad.docker_ubuntu

ansible-playbook -i inventory/vagrant deploy_docker.yml
```

Feel free to poke around, create issues if you have feedback/questions.




