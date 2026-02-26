# Enterprise Branch Network Design & Security Implementation

## 📌 Project Overview

Designed and implemented a simulated enterprise branch network in Cisco Packet Tracer demonstrating routing, switching, VLAN segmentation, WAN connectivity, and ACL-based security.

The topology replicates a real-world Head Office ↔ Branch architecture with department isolation and controlled server access.

---

## 🧱 Network Topology

**Devices Used**

* 2 × Cisco 2911 Routers
* 2 × Cisco 2960 Switches
* 4 × PCs
* 1 × Server
* Serial WAN Link

**Topology Flow**

Branch VLAN Users → Inter-VLAN Routing → WAN → Head Office → Server

*(See topology image in `/topology` folder)*

---

## 🌐 IP Addressing Scheme

| Device | IP Address    | Network |
| ------ | ------------- | ------- |
| HR PC  | 192.168.10.10 | VLAN 10 |
| IT PC  | 192.168.20.10 | VLAN 20 |
| HO PC  | 192.168.30.10 | HO LAN  |
| Server | 192.168.30.20 | HO LAN  |
| R1 WAN | 10.0.0.1      | /30     |
| R2 WAN | 10.0.0.2      | /30     |

---

## 🔧 Configurations Implemented

### VLAN Segmentation

* VLAN 10 → HR
* VLAN 20 → IT
* Access port assignment
* 802.1Q trunking

### Inter-VLAN Routing

* Router-on-a-Stick
* Subinterfaces with dot1Q encapsulation

### WAN Connectivity

* Serial DCE/DTE
* Clock rate configuration
* /30 addressing

### Dynamic Routing

* OSPF Area 0
* Multi-network advertisement

### ACL Security

* IT denied Server access
* HR allowed Server access

---

## 🔒 Security Policy

| Source  | Destination | Action  |
| ------- | ----------- | ------- |
| HR VLAN | Server      | Allowed |
| IT VLAN | Server      | Denied  |

---

## 🧪 Verification Commands

```
show ip route
show ip interface brief
show vlan brief
show access-lists
ping
tracert
```

---

## 📂 Repository Contents

* `/configs` → Device configurations
* `/screenshots` → Ping & verification proof
* `/topology` → Network diagram
* `/project-file` → Packet Tracer lab

---

## 🎯 Skills Demonstrated

* VLAN Design
* Inter-VLAN Routing
* OSPF Routing
* WAN Configuration
* ACL Security
* Network Troubleshooting

---

## 👤 Author

**Kathiravan K B**
Networking & Telecom

LinkedIn: https://www.linkedin.com/in/kathiravan-k-b-4b7168328/

Email: kbkathiravan06@gmail.com
