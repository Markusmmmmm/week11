Create ssh key pair

```
ssh-keygen -t rsa -b 4096 -f ~/.ssh/aws-key
```

import key pair

```
./import_lab_key ~/.ssh/aws-key
```

run terrafrom configuration

```
cd terraform
terraform init 
terraform validate .
terraform apply 
```

Install Required Dependencies for Ansible

```
sudo apt update && sudo apt install -y ansible
pip install python3-boto3

```

Navigate to ansible/roles/ and create the directory structure:

```
cd ansible/roles
ansible-galaxy init frontend
ansible-galaxy init backend
```

Run Ansible Playbook:

```
ansible-playbook playbook.yml --verbose
```
![alt text](victory_screenshot.png)
