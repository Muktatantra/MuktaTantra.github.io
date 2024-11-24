# Server Setup and OS Deployment: A Step-by-Step Guide

This document outlines the process of preparing a server for project deployment, including the steps taken to overcome challenges encountered during the setup.

## Step 1: Creating a Bootable Ubuntu Flash Drive

To begin, we needed to create a bootable Ubuntu flash drive to install the operating system on the server. We used the following tools and resources:

  * **BalenaEtcher:** This free and open-source image writer simplifies the process of creating bootable USB drives. You can download it from the official website: [https://www.balena.io/etcher/](https://www.google.com/url?sa=E&source=gmail&q=https://www.balena.io/etcher/)
  * **Ubuntu ISO:** The ISO image of the desired Ubuntu server distribution can be downloaded from the official Ubuntu website: [https://ubuntu.com/download/server](https://www.google.com/url?sa=E&source=gmail&q=https://ubuntu.com/download/server)

**Procedure:**

1.  Download and install BalenaEtcher.
2.  Download the Ubuntu server ISO image.
3.  Insert a USB flash drive into your computer.
4.  Open BalenaEtcher and select the downloaded Ubuntu ISO image as the source.
5.  Choose the USB flash drive as the target device.
6.  Click "Flash!" to start the process. BalenaEtcher will format the USB drive and write the ISO image to it.

## Step 2: Identifying Storage Requirements

Upon inspecting the server, we discovered it lacked internal storage for the OS deployment. This necessitated the purchase of an external storage solution.

## Step 3: Selecting and Installing Storage

We opted for a Kingston SSD with a SATA III interface due to its speed and compatibility.

**Challenge:** The server was equipped with SAS ports instead of SATA ports.

**Solution:** We used a SATA to SAS adapter to connect the SSD to a SAS port on the server.

**Procedure:**

1.  Connect the SATA SSD to the SATA to SAS adapter.
2.  Insert the adapter into an available SAS port on the server.

## Step 4: Configuring Storage

After physically installing the SSD, it needed to be configured within the server's RAID controller.

**Procedure:**

1.  Access the HP Smart Array Configuration Manager (usually accessed during server startup via a specific key combination, e.g., F8).
2.  Create a new logical drive.
3.  Select the newly detected SSD as the physical drive for the logical drive.
4.  Configure RAID level (if applicable) and assign the desired capacity to the logical drive.
5.  Save the configuration and exit the HP Smart Array Configuration Manager.

## Step 5: OS Deployment

With the storage configured, we proceeded with the Ubuntu server installation.

**Procedure:**

1.  Boot the server from the bootable Ubuntu USB drive created in Step 1.
2.  Follow the on-screen prompts to install Ubuntu server.
3.  During the installation process, select the newly created logical drive as the installation destination.
4.  Complete the installation and reboot the server.

## Further Steps:

This document provides a foundation for server setup and OS deployment. Further steps may include:

  * **Network Configuration:** Setting up static IP addresses, DNS servers, and hostname.
  * **User Management:** Creating user accounts and assigning appropriate permissions.
  * **Security Hardening:** Implementing firewalls, security updates, and other security measures.
  * **Software Installation:** Installing necessary software packages and applications for the project.
  * **Project Deployment:** Deploying the project code and configuring the environment.

This documentation will be updated as we progress through the server setup and project deployment.
