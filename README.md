# Setting Up Nginx Docker Container on an Ubuntu 22.04 EC2 Instance using Ansible playbook
This documentation provides comprehensive instructions for setting up an Nginx Docker container on an Ubuntu 22.04 EC2 instance using Ansible
# What is the Ansible playbook?
An Ansible playbook is an organized unit of scripts that defines the tasks involved in managing a system configuration. Playbooks are like step-by-step instructions for automating tasks on multiple servers. They make it easy to set up, configure, and manage servers without manual work
# Prerequisites
Before you begin, make sure you have the following:

• An AWS EC2 instance running Ubuntu 22.04.

• SSH access to the EC2 instance.

# Step 1: Clone the Ansible Playbook Repository
Clone the Repository:
Open your terminal or SSH into your EC2 instance if you prefer to work directly. Clone the Ansible playbook repository to your machine or instance.
https://github.com/Saiprasad690/Nginx-docker-container.git

In order to update and install required packages. Follow the commands below
```bash
sudo apt update
```
```bash
sudo apt upgrade
```
```bash
sudo apt install docker.io
```
```bash
sudo apt install ansible
```
```bash
sudo apt install python3
```
To verify the version of Python
```bash
python3 --version
```
```bash
sudo apt install python3-pip
```
# Step 2: Create an ansible playbook file and give a name as Nginx-docker-container.yaml
Mentioned the playbook file in another file as Demo.yaml
# Step 3: Run the Ansible Playbook
Execute the Ansible Playbook:

Run the Ansible playbook using the following command:
```bash
ansible-playbook nginx-docker-container.yaml
```
This command will run the playbook, which does the following:

Installs Docker on the EC2 instance.
Performs a Docker login, prompting you for your Docker Hub credentials.
Spins up an Nginx container with port 443 open.
Note: If Docker is already installed on your EC2 instance, the playbook will not reinstall it.
# Step 4: Accessing the Nginx Container
Once the playbook has been completed successfully, you can access the Nginx container via a web browser. Open a web browser and navigate to:
Public IP of the instance and followed by port:443
```bash
For eg: 3.80.40.52:443
```
Replace your_ec2_instance_ip with the IP address of your EC2 instance. You should see the default Nginx welcome page.
# Step 5: Removing the Nginx Container
To remove the Nginx container, use the following command on your EC2 instance:
```bash
docker stop nginx-example-docker
docker rm nginx-example-docker
```
That's it! You've successfully set up a Nginx Docker container on your Ubuntu 22.04 EC2 instance using Ansible playbook
