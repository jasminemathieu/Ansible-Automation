# Ansible Automation

<div align="center">
  <img src="https://imgur.com/2IR1Jcq.jpg" height="120" alt="linux logo"  />
  <img width="36" />
</div>

## Introduction

This project aims to automate tasks related to managing Linux servers deployed by Azure Virtual Machines (VMs) using Ansible. We’ll integrate VMware components and leverage the power of Ansible playbooks to streamline VM provisioning, configuration, and maintenance.

### Components used:

    Azure Virtual Machines: Our target infrastructure for deploying and managing Linux servers
    VMware: We’ll use VMware tools to enhance VM performance, security, and scalability.
    Ansible: Our automation engine for orchestrating tasks across VMs.
    PPA (Personal Package Archive): A repository for additional software packages.

## Project Steps
### 1. Install PPA Repository

First, let’s set up the PPA repository:

![installing ppa](https://imgur.com/W4Xxo2h.jpg) 

### 2. Update System and Install Ansible

 We will complete this step running the following commands:
  # 
  
    Update the system
    sudo apt update

    Install Ansible
    sudo apt install ansible


![installing ansible](https://imgur.com/hNG3F4z.jpg) 

### 3. Clone Ansible Playbook

Next, clone the Ansible playbook repository and generate an SSH key pair:

![clone pb](https://imgur.com/PbML0P5.jpg) 

Here, we verify that the pair key has been created as reflected below.

![keygen](https://imgur.com/MPjs9Bp.jpg) 

### 4. Share Public Key with Node(s)

Copy the public key to the target node(s). For this project we created 1 node.

![copy key](https://imgur.com/T31l6c7.jpg) 

Verify that the public key is copied successfully:

![check public key](https://imgur.com/uhwiwXm.jpg) 

### 5. Modify Inventory and Playbook

Next, we will update the playbook `playbook.yml` to define tasks for our project and edit the inventory file `inventory.yml` to include node server details: 

![inv mod](https://imgur.com/qogTyaH.jpg) 

![inv mod2](https://imgur.com/Z9bDzEP.jpg) 

### 6. Run the Playbook

Execute the playbook to automate our desired tasks using command `ansible-playbook -i inventory.yml playbook.yml`:

![autom test](https://imgur.com/nlpbPdK.jpg)  

## Conclusion

By following these steps, we were able to enhance our Linux server(s) using Ansible and VMware components. The benefit to using Ansible is we can customize our playbooks further based on project requirements.
