# My-Playbook ✅

Automation with Ansible Playbook 🛠️⚙️💡

## Getting started

- [ ] share ssh-key to all hosts to configure
```
ssh-keygen #on all host where you want to connect via ssh
ssh-copy-id username@ip-addr #ip-addr of host where you generate ssh key
```

- [ ] And you are now able to connect to those hosts, try the command below to test the connection
```
ansible -m ping -i inventory all
```

- [ ] first method by creating encrypting variable and store the encrypt var in your project
```
ansible-vault encrypt_string 'sudo_password_val' --ask-vault-pass  --name 'sudo_password'
ansible-vault encrypt_string 'host_password_val' --ask-vault-pass  --name 'host_password'
```

- [ ] second method by creating a vault file to store all sensible information
- cmd to create a vault file
```
ansible-vault create group_vars/all/vault
```
- cmd to edit your vault file
```
ansible-vault edit group_vars/all/vault
```

- [ ] Run a playbook 
- directly enter the vault pwd in terminal when using this cmd
```
ansible-playbook -i inventory site.yml --ask-vault-password
```

- with this cmd you have to create a file ( exple .passwd.py ) who will content your vault password
```
ansible-playbook -i inventory site.yml --vault-password-file .passwd.py
```
don't forget to add vault password file to .gitignore

## Install and configure an runner host

- [ ] Run the playbook
```
ansible-playbook -i inventory site_runner.yml --vault-password-file .passwd.py
```

## Install and configure an kubernetes Cluster

- [ ] Run the playbook
```
ansible-playbook -i inventory site_staging.yml --vault-password-file .passwd.py
```