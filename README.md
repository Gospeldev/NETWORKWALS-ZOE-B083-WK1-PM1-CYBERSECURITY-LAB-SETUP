
# CYBERSECURITY LAB ENVIROMENT SETUP

# Project Overview
This project documents the setup of a personal cybersecurity lab using
Oracle VirtualBox and Kali Linux. The lab provides an isolated
virtual environment for practicing cybersecurity concepts, networking,
system administration, and security tools without directly affecting the
host computer.

The project focuses on configuring Kali Linux as a virtual machine,
establishing network connectivity, and preparing the environment for
future cybersecurity experiments and hands-on learning.

# Objectives
The main objectives of this project were to:

Install and configure Oracle VirtualBox on the host computer.

Set up a Kali Linux virtual machine using the VirtualBox-compatible
Kali Linux image.

Configure the virtual machine's hardware and network settings.

Configure the VM network adapter using VirtualBox NAT networking.

Verify that the virtual network adapter is enabled and that the
virtual cable is connected.

Configure and troubleshoot the Kali Linux wired network connection.

Verify the VM's IP address and default gateway using Linux
networking commands.

Test network connectivity between the Kali Linux VM and external
network resources.

Document problems encountered during the setup and the solutions
used to troubleshoot them.

# Purpose of the Lab
The purpose of this lab is to create a controlled and isolated
environment where cybersecurity concepts can be learned and tested
practically.

The lab can be used for activities such as:

Network traffic analysis

Linux command-line practice

Network reconnaissance in an authorized environment

Vulnerability assessment

Security monitoring and log analysis

Learning cybersecurity tools such as Wireshark, Nmap, tcpdump, and
other security utilities

Practicing defensive security techniques

Building practical experience for cybersecurity and SOC analyst
roles

# Lab Setup Procedure

## step 1: Install Oracle VirtualBox
Downloaded and installed Oracle VirtualBox on the host computer.

Opened VirtualBox and verified that the application was working
correctly.

Prepared VirtualBox to host the Kali Linux virtual machine.

Ensured that the host computer had sufficient storage and system
resources available for the VM.
<img width="1920" height="1020" alt="virtual_box download" src="https://github.com/user-attachments/assets/1c96af16-1e98-40e1-a8d4-5fb37bb54c7a" />

## Set Up the Kali Linux Virtual Machine
Imported/configured the Kali Linux virtual machine in VirtualBox.

Verified the VM's basic hardware configuration.

Allocated appropriate memory and processor resources to the VM.

Started the Kali Linux virtual machine.

Confirmed that Kali Linux booted successfully and that the desktop
environment was accessible.
<img width="974" height="608" alt="kali_linux" src="https://github.com/user-attachments/assets/ebc36d11-0f30-45a1-a503-e7d5f7df4b75" />

## Step 3: Configure the Virtual Network Adapter
Opened the Kali VM's Settings → Network → Adapter 1 in
VirtualBox.

Enabled the network adapter.

Configured the adapter to use NAT Network.

Selected the NatNetwork network.

Used the Intel PRO/1000 MT Desktop (82540EM) virtual adapter
type.

Enabled Cable Connected so that the virtual machine could detect
the network interface.

Verified that the network adapter was available to Kali Linux.
<img width="961" height="558" alt="NAT_Network_setup" src="https://github.com/user-attachments/assets/72048509-1f7c-4989-b68e-6fab1681c8fa" />

## Step 4: Configure and Verify the Kali Network Connection
<img width="1920" height="991" alt="kali_linux_network_settings" src="https://github.com/user-attachments/assets/ae77e930-3b13-44bf-8251-41f42e2d66f4" />

## Test Network Connectivity
Verified that the Kali Linux network interface was active.

Checked that the VM received an appropriate IP address from the NAT
network.

Verified the default gateway using:

ip route

Tested connectivity to an external IP address:

ping -c 4 8.8.8.8

Tested DNS resolution by running:

ping -c 4 google.com

Confirmed that the virtual machine could communicate with external
network resources.

Documented the final network configuration for future cybersecurity
lab exercises.
<img width="1920" height="991" alt="kali-linux_bash_shell" src="https://github.com/user-attachments/assets/bb1c28b2-b5f6-46a9-b3a4-5a7ea1d82531" />

# Problems Encountered and Solutions

## Problem 1: Wired Connection 1 showed as disconnected
Kali Linux displayed Wired Connection 1 as disconnected, even though
the VirtualBox network adapter was enabled.

Solution:
Checked the VirtualBox network configuration and confirmed that:

Enable Network Adapter was selected.

The adapter was attached to a NAT-based network.

Cable Connected was enabled.

The Kali NetworkManager connection was then checked and activated when
necessary using:

nmcli connection up "Wired connection 1"

## Problem 2: Confusion between NAT and NAT Network
The VirtualBox adapter was configured as NAT Network, which
initially caused uncertainty about whether the network needed to have
previously been used by the host computer to access the Internet.

Solution:
Established the distinction between the two VirtualBox networking modes:

NAT: Provides Internet access to the VM through VirtualBox's
built-in NAT service.

NAT Network: Provides a shared virtual network that can allow
multiple VMs to communicate while also providing NAT-based Internet
access when properly configured.

The NatNetwork configuration was checked to ensure that the virtual
network was available and properly configured.

# Conclusion
The project established a functional foundation for a virtual
cybersecurity laboratory using VirtualBox and Kali Linux. The setup
process involved configuring the virtual machine, establishing NAT-based
networking, troubleshooting the Kali wired connection, and verifying
network connectivity.

This environment can now be expanded with additional virtual machines
and cybersecurity tools to support practical exercises in networking,
penetration testing, vulnerability assessment, security monitoring, and
SOC analysis.

# 👨‍🦰 Author
### Chidozie Zoe Gospel
Cybersecurity Professional B083

LinkedIn: https://www.linkedin.com/in/chidozie-gospel/

# Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup |  Repository: Github
