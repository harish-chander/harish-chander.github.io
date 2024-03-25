+++
title = '3cxinstallation'
date = 2024-03-25T13:00:14+04:00
draft = true
+++

# Installation of 3CX on Debian 12

## Introduction
 This guide will help you to install 3CX on Debian 12. 3CX is a software-based private branch exchange (PBX) based on the SIP (Session Initiation Protocol) standard. It enables extensions to make calls via the public switched telephone network (PSTN) or via Voice over Internet Protocol (VoIP) services.

 For this guide, we will use Debian 12 as the operating system. Debian is a free and open-source operating system that is widely used in the server environment. It is known for its stability, security, and ease of use.

 more information about 3CX, you can visit the official website at [3CX](https://www.3cx.com/).

## Prerequisites
    Before you start with the installation of 3CX on Debian 12, you need to have the following prerequisites:
    - A server or virtual machine running Debian 12.
    - Root access to the server or virtual machine.
    - A valid FQDN (Fully Qualified Domain Name) for the server. or you can use the free domain provided by 3cx wizard
    - A valid SSL certificate for the FQDN. or you can use the free SSL certificate provided by 3cx wizard
    - A valid license key for 3CX. You can get a free license key by signing up on the 3CX website.
    - A stable internet connection.
    - Basic knowledge of Linux and the command line.
    - Basic knowledge of networking and VoIP.
  
## Step 1: Update the System
    Before you start with the installation of 3CX, it is recommended to update the system to the latest version. You can do this by running the following commands:
    ```bash
    sudo apt update
    sudo apt upgrade
    ```
    This will update the package list and upgrade the installed packages to the latest version.

## Step 2: Install Dependencies
    3CX requires some dependencies to be installed on the system. You can install them by running the following command:
    ```bash
    sudo apt install curl wget gnupg2 dirmngr
    ```
    This will install the required dependencies on the system.

## Step 3: Download the 3CX Installation Script
    3CX provides an installation script that will automate the installation process. You can download the script by running the following command:
    ```bash
    curl -O https://downloads-global.3cx.com/downloads/3cxpbx/public.key && sudo apt-key add public.key
    ```
    This will download the installation script and add the public key to the system.

## Step 4: Install 3CX
    Once you have downloaded the installation script, you can install 3CX by running the following command:
    ```bash
    echo "deb http://downloads-global.3cx.com/downloads/debian stretch main" | sudo tee /etc/apt/sources.list.d/3cxpbx.list
    sudo apt update
    sudo apt install 3cxpbx
    ```
    This will add the 3CX repository to the system and install 3CX on Debian 12.

## Step 5: Configure 3CX
    This below step is only requried if you are want to run the setup wizard again.
    After the installation is complete, you can configure 3CX by running the following command:
    ```bash
    sudo /usr/sbin/3CXWizard
    ```
    This will start the 3CX configuration wizard, where you can set up the basic configuration of 3CX.

## Step 6: Access 3CX Web Interface
    Once the configuration is complete, you can access the 3CX web interface by opening a web browser and navigating to `https://<your-server-ip>:5051`. You will be prompted to log in with the username and password you set during the configuration process.

## Conclusion
    In this guide, you have learned how to install 3CX on Debian 12. You can now start using 3CX to make calls via the public switched telephone network (PSTN) or via Voice over Internet Protocol (VoIP) services. If you have any questions or feedback, feel free to leave a comment below.

    Thank you for reading!

    

