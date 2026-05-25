# packet-tracer-enterprise-ISP-network
Enterprise Network with OSPF, NAT and 3G/4G Cellular Tower Network - Cisco Packet Tracer Project 

# 📱 Enterprise 4G/3G Network with OSPF, NAT & Wireless

![Packet Tracer](https://img.shields.io/badge/Packet%20Tracer-8.x-blue)
![Cisco](https://img.shields.io/badge/Cisco-CCNA-green)
![OSPF](https://img.shields.io/badge/Routing-OSPFv2-purple)
![NAT](https://img.shields.io/badge/NAT-PAT-orange)
![Wireless](https://img.shields.io/badge/Wireless-802.11n-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📋 Project Overview

This project simulates a complete **Enterprise Network** connecting a **remote branch office** to **ISP/Internet** using **3G/4G cellular WAN connectivity**. The network features **OSPF routing** between sites, **NAT/PAT** for internet access, and **secure wireless connectivity** for end users.

### 🎯 Key Features

| Feature | Technology Used |
|---------|-----------------|
| **WAN Connectivity** | 3G/4G Cellular (simulated via ISP Router) |
| **Routing Protocol** | OSPF (Multi-Area: Area 0 & Area 1) |
| **Internet Access** | PAT (NAT Overload) on Branch Router |
| **IP Management** | DHCP for wired and wireless clients |
| **Wireless Network** | 802.11n WAP with WPA2-PSK Security |
| **Network Architecture** | Hierarchical Enterprise Design |

### 📊 IP Addressing Scheme

| Device | Interface | IP Address | Subnet Mask | Network | Purpose |
|--------|-----------|------------|-------------|---------|---------|
| **ISP Router** | Fa0/0 | 192.168.10.1 | 255.255.255.0 | 192.168.10.0/24 | 3G/4G Gateway |
| **ISP Router** | Loopback0 | 8.8.8.8 | 255.255.255.255 | - | Internet Simulation |
| **Branch Router** | Gig0/0 | 192.168.100.2 | 255.255.255.252 | 192.168.100.0/30 | Link to Core |
| **Branch Router** | Gig0/1 | DHCP (192.168.10.x) | 255.255.255.0 | 192.168.10.0/24 | ISP Connection |
| **Branch Router** | Gig0/2 | 192.168.2.1 | 255.255.255.0 | 192.168.2.0/24 | Wireless LAN |
| **Branch Router** | Gig0/3 | 192.168.1.1 | 255.255.255.0 | 192.168.1.0/24 | Wired LAN |
| **Core Switch** | VLAN 1 | 192.168.100.3 | 255.255.255.252 | 192.168.100.0/30 | Management |
| **WAP-PT** | LAN | 192.168.2.2 | 255.255.255.0 | 192.168.2.0/24 | Wireless AP |
| **Wired PC** | DHCP | 192.168.1.50-200 | 255.255.255.0 | 192.168.1.0/24 | Employee PC |
| **Wireless Laptop** | DHCP | 192.168.2.50-200 | 255.255.255.0 | 192.168.2.0/24 | Mobile User |

### 🔧 Technologies Implemented

| Technology | Configuration | Purpose |
|------------|---------------|---------|
| **OSPF Multi-Area** | Area 0 (Backbone), Area 1 (Branch) | Dynamic routing between sites |
| **NAT/PAT** | Overload on Gig0/1 | Internet access for internal users |
| **DHCP** | Pools for wired/wireless | Automatic IP assignment |
| **3G/4G WAN** | ISP Router simulation | Cellular internet connectivity |
| **Wireless Security** | WPA2-PSK, AES | Secure mobile access |
| **Enterprise Switching** | Layer 2 connectivity | Internal network distribution |

📜 License
MIT License - See LICENSE file

👤 Author
Hiran Dharmapala