# Firewall Assignment

## Overview
This repository contains the configuration and testing of a basic firewall rule on a local server. The firewall was set up using UFW (Uncomplicated Firewall) on Linux. The goal was to allow secure SSH access while blocking all other incoming traffic, and permitting outgoing traffic.

## Configuration
The following steps were performed:
1. Enabled UFW:
   ```bash
   sudo ufw enable
   sudo ufw allow 22/tcp
   sudo ufw default deny incoming
   sudo ufw default allow outgoing
   sudo ufw status numbered
   Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere
22/tcp (v6)                ALLOW       Anywhere (v6)
Anywhere                   DENY        Anywhere
Anywhere (v6)              DENY        Anywhere (v6)
