# Configure Remote Device

## Overview


## Setup

### Install dependencies

```sh
sudo apt update
sudo apt install ansible -y
sudo apt install sshpass -y
```


### Check for remote devices
1. Add in `inventory.ini` the remote devices with its dynamic IP
2. Test if connected: `ansible -i inventory.ini rpi -m ping`


### Configure a remote
1. Set the parameters in `configure.yml`
2. Run the ansible playbook: `ansible-playbook -i inventory.ini -K configure.yml`
3. In `inventory.ini` replace dynamic IP with the new static IP


### Install a service

```sh
ansible-playbook -i inventory.ini -K --ask-vault-pass install-service.yml
ansible-playbook -i inventory.ini -K --ask-vault-pass update-service.yml
ansible-playbook -i inventory.ini -K --ask-vault-pass check-service.yml
```



