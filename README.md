# Ansible Automation

<div align="center">
  <img src="https://imgur.com/2IR1Jcq.jpg" height="120" alt="linux logo"  />
  <img width="36" />
</div>

## Introduction

This project aims to automate tasks related to managing Linux servers deployed by Azure Virtual Machines (VMs) using Ansible. We’ll integrate VMware components and leverage the power of Ansible playbooks to streamline VM provisioning, configuration, and maintenance.

### Components used:

    Azure Virtual Machines: Our target infrastructure for deploying and managing VMs.
    VMware: We’ll use VMware tools to enhance VM performance, security, and scalability.
    Ansible: Our automation engine for orchestrating tasks across VMs.
    PPA (Personal Package Archive): A repository for additional software packages.

## Project Steps
### 1. Install PPA Repository

First, let’s set up the PPA repository:

![installing ppa](https://imgur.com/xn7vUhr.jpg) 

### 2. System Update and Install Ansible

 We will complete this step running the following commands
  # 
  
    Update the system
    sudo apt update

    Install Ansible
    sudo apt install ansible


![installing ansible](https://imgur.com/UlNQS8Q.jpg) 

### 3. Clone Ansible Playbook

Next, clone the Ansible playbook repository and generate an SSH key pair:

![clone pb](https://imgur.com/0I00N2y.jpg) 

### 4. Generate SSH Key Pair

![keygen](https://imgur.com/UD7cs84.jpg) 

### 5. Share Public Key with Node(s)

Copy the public key to the target node(s). For this project we created 1 node.

![copy key](https://imgur.com/6b7MXOs.jpg) 

Verify that the public key is copied successfully:

![check public key](https://imgur.com/myrzhbY.jpg) 

### 6. Modify Inventory and Playbook

Update the playbook `playbook.yml` to define tasks for your project and edit the inventory file `inventory.yml` to include node server details: 

![inv mod](https://imgur.com/eIdvUYj.jpg) 

![inv mod2](https://imgur.com/pP53UvQ.jpg) 

### 7. Run the Playbook

Execute the playbook to automate your desired tasks using command `ansible-playbook -i inventory.ini playbook.yml`:

![autom test](https://imgur.com/18EVv4r.jpg)  

## Conclusion

By following these steps, we were able to enhance our Linux server(s) using Ansible and VMware components. The benefit to using Ansible is we can customize our playbooks further based on project requirements.
