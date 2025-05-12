# TNE30023
Advanced Switching 


## Overview

This repo walks you through securing a small network using Cisco IOS:

- **Switch security** (port security, BPDU guard, storm control)  
- **Router hardening** (SSH, AAA, NTP, SNMP)  
- **IPsec VPN** (site-to-site tunnel between R1 ↔ R2)  
- **Zone-Based Policy Firewall** (ZPF on R3)

---

## Topology & Addressing

![image](https://github.com/user-attachments/assets/976ad84d-d83d-47de-b92b-40910333b2a8)


| Device | Interface      | IP Address       | Subnet Mask     | Description           |
|:------:|:---------------|:-----------------|:----------------|:----------------------|
| R1     | G0/0           | 64.100.1.1       | 255.255.255.252 | Link to R2            |
| R1     | G0/1           | 192.168.1.1      | 255.255.255.0   | LAN                   |
| R2     | G0/0           | 64.100.1.2       | 255.255.255.252 | Link to R1            |
| R2     | G0/1           | 64.100.3.2       | 255.255.255.252 | Link to R3            |
| R3     | G0/0           | 64.100.3.1       | 255.255.255.252 | Link to R2            |
| R3     | G0/1.3 (VLAN3) | 172.16.3.1       | 255.255.255.0   | User VLAN             |
| S2     | VLAN 3         | 172.16.3.2       | 255.255.255.0   | Access switch S2      |
| S3     | VLAN 3         | 172.16.3.3       | 255.255.255.0   | Access switch S3      |

---
