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
git clone https://github.com/yourusername/ansible-nginx-docker.git
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
