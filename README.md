# Configure Remote Device


Install Ansible:
sudo apt update
sudo apt install ansible -y
sudo apt install sshpass -y


Check
ansible -i inventory.ini rpi -m ping


Ansible
ansible-playbook -i inventory.ini -K configure.yml
