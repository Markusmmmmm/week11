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
<img width="315" alt="Screenshot 2025-03-21 152122" src="https://github.com/user-attachments/assets/870f69a2-d657-42ad-9f77-a4bc1796d479" />
