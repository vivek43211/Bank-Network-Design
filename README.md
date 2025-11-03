# Bank-Network-Design
Bank Network Design &amp; Implementation Project on Packet Tracer
# 🏦 Bank System Network Design (Project #5)

## 📘 Overview
This project, titled **“Design and Implementation of a Bank System Network Design,”** was developed as part of a case study for **Radeon Company Ltd.**, a U.S.-based banking and insurance firm expanding into Nairobi, Kenya.  

The objective was to design and implement a **four-story enterprise network** that meets real-world standards for scalability, security, and efficient communication using **Cisco Packet Tracer**.

---

## 🏗️ Project Description
**Radeon Company Ltd.** required a fully functional, secure, and scalable network for their new Nairobi branch.  
The network had to connect all departments across four floors, provide wired and wireless connectivity, secure remote access, and ensure centralized management.

The design follows the **Hierarchical Network Model** (Core, Distribution, and Access Layers) for optimal performance and manageability.

---

## 🏢 Building Structure and Department Allocation

| Floor | Departments |
|-------|--------------|
| **1st Floor** | Management, Research, HR |
| **2nd Floor** | Marketing, Accounting, Finance |
| **3rd Floor** | Customer Care, Guest Area, Loans & Admin |
| **4th Floor** | ICT, Server Room (DHCP, HTTP, E-mail Servers) |

Each department was assigned a **dedicated VLAN** for logical segmentation and enhanced security.

---

## 🧠 Design Goals and Requirements

✅ Provide inter-department communication through **OSPF Routing**  
✅ Ensure **automatic IP addressing** via centralized DHCP  
✅ Secure remote device access with **SSH configuration**  
✅ Set up **VLANs and WLANs** for every department  
✅ Implement **Port Security** to restrict unauthorized access  
✅ Configure **HTTP and E-mail servers** for internal communication  
✅ Enable **Inter-VLAN routing** using Layer 3 switches  
✅ Use **Banner messages**, **password encryption**, and **login security** on all devices  
✅ Disable **domain lookup** for faster CLI interaction  

---

## 🌐 Network Topology

Below is the visual representation of the complete network topology designed in **Cisco Packet Tracer**:

![Bank Networking Design](Bank%20Networking%20pic.png)

---

## ⚙️ Technologies & Tools Used

| Category | Tools/Protocols |
|-----------|----------------|
| **Simulation Software** | Cisco Packet Tracer |
| **Modeling Tools** | MS Visio / Draw.io / Visual Paradigm |
| **Routing Protocol** | OSPF (Open Shortest Path First) |
| **Addressing** | IPv4 Subnetting (Base: `192.168.10.0/24`) |
| **DHCP Services** | Centralized DHCP Server (Server Room) |
| **Security** | SSH, Port Security (Sticky MAC, Shutdown Mode) |
| **VLAN Configuration** | VLANs 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120 |
| **Servers Implemented** | HTTP, Email, DHCP |
| **Wireless** | Cisco Access Points per department |
| **Switches/Routers** | Cisco 2960-24TT, 3560-24PS, and 2911 Routers |

---

## 🧩 VLAN and Subnet Planning

The base network `192.168.10.0/24` was subnetted based on departmental host requirements.  
Each department supports ~60 users (wired + wireless), so subnetting was done to accommodate growth.

| VLAN | Department | Subnet | Subnet Mask | Usable Range | Broadcast |
|------|-------------|---------|--------------|---------------|------------|
| 10 | Management | 192.168.10.0 | /26 | 192.168.10.1 – 192.168.10.62 | 192.168.10.63 |
| 20 | Research | 192.168.10.64 | /26 | 192.168.10.65 – 192.168.10.126 | 192.168.10.127 |
| 30 | HR | 192.168.10.128 | /26 | 192.168.10.129 – 192.168.10.190 | 192.168.10.191 |
| 40 | Marketing | 192.168.10.192 | /26 | 192.168.10.193 – 192.168.10.254 | 192.168.10.255 |
| 50 | Accounting | 192.168.11.0 | /26 | 192.168.11.1 – 192.168.11.62 | 192.168.11.63 |
| 60 | Finance | 192.168.11.64 | /26 | 192.168.11.65 – 192.168.11.126 | 192.168.11.127 |
| 70 | Loans | 192.168.11.128 | /26 | 192.168.11.129 – 192.168.11.190 | 192.168.11.191 |
| 80 | Customer Care | 192.168.11.192 | /26 | 192.168.11.193 – 192.168.11.254 | 192.168.11.255 |
| 90 | Guest Area | 192.168.12.0 | /26 | 192.168.12.1 – 192.168.12.62 | 192.168.12.63 |
| 100 | Admin | 192.168.12.64 | /26 | 192.168.12.65 – 192.168.12.126 | 192.168.12.127 |
| 110 | ICT | 192.168.12.128 | /26 | 192.168.12.129 – 192.168.12.190 | 192.168.12.191 |
| 120 | Server Room | 192.168.12.192 | /26 | 192.168.12.193 – 192.168.12.254 | 192.168.12.255 |

---


