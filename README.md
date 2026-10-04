# DigitalOcean Droplet Deployment Guide

## Overview
This document provides a detailed, step-by-step procedure for provisioning a new virtual machine (Droplet) on the DigitalOcean cloud platform and establishing a secure connection to it.

## Prerequisites
- An active DigitalOcean account.
- An SSH client available on your local machine.
- An SSH key pair generated for secure authentication.

## Step-by-Step Instructions

### 1. Accessing the Control Panel
- Navigate to the DigitalOcean Control Panel and log in using your account credentials.
- Click the **Create** button located in the top navigation bar.
- Select **Droplets** from the dropdown menu to initiate the deployment wizard.

### 2. Configuring the Droplet
- **Choose Region**: Select a datacenter region that is geographically closest to your primary user base to minimize latency.
- **Choose Image**: Select the desired operating system. A standard choice is **Ubuntu 24.04 (LTS) x64**.
- **Choose Size**: Select the **Basic** plan, then choose the appropriate CPU and Memory specifications (e.g., Regular Intel with 1GB RAM) based on the application workload.
- **Choose Authentication Method**: Select **SSH Key**. Click **New SSH Key** and paste your public SSH key. This is a mandatory step for adhering to security best practices.

### 3. Finalizing and Provisioning
- **Finalize Details**: Under the "Choose a hostname" section, assign a descriptive and standardized name to the Droplet (e.g., `web-server-sgp1-01`).
- **Tags**: Apply relevant tags for easier filtering and management.
- Click the **Create Droplet** button at the bottom of the page.
- The provisioning process will take a few moments. Once completed, the dashboard will display the new Droplet along with its assigned public IPv4 address.

### 4. Establishing a Connection
After the Droplet is fully provisioned and active, open your local terminal to connect via SSH:

```bash
ssh root@<YOUR_DROPLET_PUBLIC_IP>
```

If this is your first time connecting, your SSH client will prompt you to verify the host key fingerprint. Type `yes` to proceed and establish the connection.

## Verification

Below is the verification of a successful Droplet creation and connection.

> **[PLACEHOLDER: Insert a screenshot of the DigitalOcean Droplet Console showing the active status and IP address, OR insert a snippet of the Terminal log demonstrating a successful SSH connection]**

***
*End of document*
