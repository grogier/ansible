# Ansible
collection of Ansible playbooks


# Setup
- install WSL
- generate keypair
- copy keypair from windows machine to wsl folder
- chmod 600 for private key


## Ansible commands from working directory 


```sh
# command to run an ansible command to a set of hosts
ansible all -i hosts -m ping
```

```sh
# use the ansible.cfg to run the ping command
ansible all -m ping
```

```sh
# use the ansible.cfg, to list the hosts
ansible all --list-hosts

```


```sh
# use the ansible.cfg to gather facts
ansible all -m gather_facts

# limit information to a specific host
ansible all --list-hosts --limit 10.0.20.10
```


## Ansible playbook command
```sh
# run a playbook
ansible-playbook linux-up-to-date.yml
```


## installing certificate to any host

rogier@Rogier-PC-2024:~/ansible/.ssh$ ssh-copy-id -i semaphore_rsa.pub rogier@10.0.0.112
