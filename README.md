# Simple Ansible playbook to create 3 ec2 intances in aws

## Install Ansible
   - To install Ansible follw the instructionsin [this link](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Create an use on aws IAM
   - In AWS console creaate a new user with Admin Privileges
   - Get the "Access key ID" and "Secret access key"
     
### Set user credentias with credentials
   ```shell
   export AWS_ACCESS_KEY_ID="put the credentiasl here"
   export AWS_SECRET_ACCESS_KEY="put the credentiasl here"

   ```

## Generate the a new Key Pair
   - Generate a new key pair in aws console, called ansible-test and download the ".pem", file;
   - Put the file inside the root of the project;
   - Execute the following command give permission and add the ssh key

   ```shell
   chmod 0400 ansible-test.pem
   ssh-add ansible-test.pem
   ```

## Edit the the vars file
   - Edit the file "roles/create/vars/main.yml" and change the "allowed_ip" to your ip in place of 0.0.0.0/32