# 🚀 VLAN Configuration Lab

## 📄 Description
A hands-on lab demonstrating how to configure VLANs on a Cisco switch using Packet Tracer.  
This lab showcases how VLANs improve network segmentation, security, and performance in enterprise environments.

---

## 🧪 Lab Overview
In this lab, a Cisco switch is configured to segment the network into three VLANs representing different departments.  
Each VLAN is assigned to specific switch ports to isolate traffic and simulate real-world departmental separation.

---

## 📊 VLANs Used

| VLAN ID | Department |
|---------|------------|
| 3       | HR         |
| 4       | FINANCE    |
| 5       | IT         |

---

## ⚙️ Configuration Steps

### 🔸 Step 1: Create VLANs and Name Them
```bash
Switch(config)# vlan 3
Switch(config-vlan)# name HR

Switch(config)# vlan 4
Switch(config-vlan)# name FINANCE
```
### 🔸 Step 2: Assign VLANs to Interfaces
```bash
Switch(config)# interface range fa0/1 - 3
Switch(config-if)# switchport access vlan 3

Switch(config)# interface range fa0/4 - 6
Switch(config-if)# switchport access vlan 4

Switch(config)# interface range fa0/10 - 13
Switch(config-if)# switchport access vlan 5
```
### 🔸 Step 3: Save Configuration
```bash
Switch# copy running-config startup-config
Switch# wr
Switch(config)# do wr
Switch(config)# do copy running-config startup-config
```
---
### 💡 Takeaway
- This setup demonstrates how VLANs can be used to simulate departmental separation in a corporate network, enhancing both security and efficiency.
- A great exercise for anyone preparing for CCNA or working in IT infrastructure!
![3](https://github.com/user-attachments/assets/02a0a254-bcbe-4f3c-92e7-f048094b3179)


Switch(config)# vlan 5
Switch(config-vlan)# name IT
