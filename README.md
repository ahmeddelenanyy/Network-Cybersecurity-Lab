# Networkwalks Internship - Week 1: Network Security Lab Setup

This repository documents the first step of my Cybersecurity Internship at NETWORKWALKS. Before starting the practical network security labs, setting up a secure and isolated virtual environment is required.

## Objective
Configuring a Kali Linux virtual machine using VirtualBox. This provides a safe, isolated lab to practice network analysis, traffic monitoring, and security configurations in the upcoming weeks.

## Prerequisites
* Oracle VM VirtualBox
* Kali Linux Pre-built VM Image (VirtualBox 64-bit)

## Virtual Machine Configuration
To make sure the VM runs smoothly during the labs, I configured it with the following resources:
* **Operating System:** Linux (Debian 64-bit)
* **RAM:** 4096 MB (4 GB)
* **Processors (CPU):** 2 Cores
* **Network Adapter:** NAT Network 

## Step-by-Step Setup

### Step 1: Importing the VM
Downloaded the pre-built Kali Linux image and imported the `.vbox` file into VirtualBox.
![Importing VM](image.png)

### Step 2: Hardware Allocation
Adjusted the system settings, allocating 4GB of RAM and 2 CPU cores to ensure good performance.
![System Configuration](image_2.png)

### Step 3: Network Configuration
Set up a dedicated **NAT Network** (10.0.0.0/24) with DHCP enabled. This is an important step for future labs to allow VMs to communicate with each other securely while maintaining internet access.
![Network Configuration](image_3.png)

### Step 4: System Update
Booted up the machine and updated the system packages to get everything ready using the terminal:
```bash
sudo apt update && sudo apt full-upgrade -y
