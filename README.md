# Ubuntu 18.04 CIS Benchmark for Ansible
Ansible role that configures Ubuntu 18.04 to CIS Benchmark v1.1.0 - https://www.cisecurity.org/benchmark/ubuntu_linux/

## Requirements
Ansible 2.4+

## Install Ansible
```
sudo apt-get update && sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update && sudo apt-get install ansible
```

## Download Role From GitHub
```
git clone https://github.com/paxdominicus/ubuntu-18.04-cis-benchmark-for-ansible.git roles/ubuntu-18.04-cis-benchmark-for-ansible
```

## Create Playbook
```
cat >>  playbook.yml << 'EOF'
---
- hosts: all
  roles:
    - ubuntu-18.04-cis-benchmark-for-ansible
EOF
```

## Configure Playbook
```
sudo nano roles/ubuntu-18.04-cis-benchmark-for-ansible/defaults/main.yml
```

## Run Playbook
```
sudo ansible-playbook -b -i "localhost," -c local playbook.yml
```
