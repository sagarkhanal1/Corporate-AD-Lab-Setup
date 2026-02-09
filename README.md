# Routing, Firewall and VLAN Segmentation with pfSense

## 📌 Project Overview

This project demonstrates the implementation of enterprise-style network segmentation using pfSense in a virtual lab environment.

The lab includes:
- pfSense Firewall
- Windows Server 2022 (Domain Controller)
- Windows 10 Client
- Kali Linux (Attacker Machine)

The objective of this project is to:

- Implement VLAN-based network segmentation
- Configure inter-VLAN routing
- Apply firewall rules to restrict lateral movement
- Configure NAT for internet access
- Validate segmentation through testing
- Analyze firewall logs for SOC monitoring scenarios

---

## 🏗 Lab Architecture

### Network Design

| VLAN | Purpose | Subnet |
|------|---------|--------|
| VLAN 10 | User Network | 192.168.10.0/24 |
| VLAN 20 | Server Network | 192.168.20.0/24 |

### Device Placement

- Windows 10 → VLAN 10
- Kali Linux → VLAN 10
- Domain Controller → VLAN 20
- pfSense → Default Gateway for all VLANs

---

## 🔧 Technologies Used

- pfSense Firewall
- Windows Server 2022
- Active Directory Domain Services
- Windows 10
- Kali Linux
- VirtualBox

---

## 🔐 Security Controls Implemented

- Inter-VLAN firewall restrictions
- Controlled AD port access (Kerberos, LDAP, SMB, DNS)
- Blocked unnecessary lateral movement
- NAT configuration for outbound traffic
- Firewall logging enabled

---

## 🧪 Validation & Testing

- Verified domain join across VLANs
- Tested blocked traffic between user and server VLAN
- Simulated lateral movement attempts from Kali
- Analyzed pfSense firewall logs

---

## 🎯 Skills Demonstrated

- Network segmentation
- Firewall configuration
- VLAN setup
- Active Directory integration
- SOC-relevant log analysis
- Enterprise-style network architecture

---

## 📈 Future Improvements

- Add IDS/IPS (Snort or Suricata)
- Integrate Wazuh for centralized logging
- Simulate privilege escalation attacks
- Implement Zero Trust model

