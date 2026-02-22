# 🛡️ Corporate Active Directory Cybersecurity Lab

A fully virtualized corporate-style lab environment built in VirtualBox for practicing Active Directory attacks, network security, and defensive monitoring.

---

## 📌 Lab Overview

This lab simulates a small corporate network with:

- Firewall segmentation
- Active Directory Domain Controller
- Domain-joined Windows client
- Attacker machine
- DHCP relay architecture

Designed for Red Team and Blue Team practice.

---

## 🏗️ Infrastructure

### 🔥 Firewall
- pfSense
- 2 NICs:
  - NAT (Internet access)
  - Internal Network (intnet)
- DHCP disabled
- DHCP Relay enabled

### 🖥️ Domain Controller
- Windows Server 2022
- Roles:
  - AD DS
  - DNS
  - DHCP
- Static IP
- Handles authentication & IP assignment

### 👤 Client Machine
- Windows 10
- Domain joined
- Receives IP via DHCP relay

### 🐉 Attacker Machine
- Kali Linux
- Used for internal penetration testing

---

## 🌐 Network Design

| Machine | Interface | Purpose |
|----------|------------|----------|
| pfSense | NAT + intnet | Firewall & Gateway |
| DC | intnet | AD, DNS, DHCP |
| Win10 | intnet | User workstation |
| Kali | intnet | Internal attacker |

---

## 🔐 Security Concepts Practiced

- Network segmentation
- DHCP relay architecture
- Active Directory management
- AD attack simulation
- Log monitoring & detection
- Lateral movement testing

---

## 🔴 Red Team Modules

- AD Enumeration
- SMB & LDAP discovery
- Kerberoasting
- AS-REP Roasting
- Pass-the-Hash
- Lateral Movement
- RDP brute force simulation


---

## 🔵 Blue Team Modules

- Windows Event Logs
- Sysmon configuration
- Brute-force detection
- Firewall log analysis
- Attack detection scenarios


---

## 🛠️ Tools Used

- VirtualBox
- pfSense
- Windows Server 2022
- Windows 10
- Kali Linux

---

## 🎯 Purpose

This lab is built to:

- Simulate real-world corporate AD environment
- Practice offensive security techniques safely
- Build defensive monitoring capabilities
- Prepare for certifications (eJPT, PNPT, OSCP, Security+)

---

## 🚀 Future Improvements

- VLAN segmentation
- DMZ implementation
- IDS/IPS integration
- SIEM deployment
- Automated attack scripts

