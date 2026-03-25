# 🔐 Enterprise Network Lab: Site-to-Site VPN

🚀 Hands-on lab simulating secure communication between two remote offices

## 🌍 Overview
This project simulates a site-to-site connection between two offices using routing and secure communication concepts.

## 🖼 Topology
![Topology](topology.png)

Topology created using Cisco Packet Tracer

## 🧰 Tools
- Cisco Packet Tracer
- CLI (Command Line Interface)

## 🧠 Network Design
- 2 Sites (Office A & Office B)
- Inter-network communication via router
- Static routing between networks

## 📊 IP Addressing

| Site | Network | Gateway |
|------|--------|--------|
| Office A | 192.168.1.0/24 | 192.168.1.1 |
| Office B | 192.168.2.0/24 | 192.168.2.1 |

---

## ⚙️ Configuration

### 🔹 Router A
```bash
conf t

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown

interface s0/0/0
ip address 10.0.0.1 255.255.255.252
no shutdown

ip route 192.168.2.0 255.255.255.0 10.0.0.2



### 🔹 Router B
```bash
conf t

interface g0/0
ip address 192.168.2.1 255.255.255.0
no shutdown

interface s0/0/0
ip address 10.0.0.2 255.255.255.252
no shutdown

ip route 192.168.1.0 255.255.255.0 10.0.0.1


🧪 Testing
Connectivity Test
Ping from Office A to Office B: SUCCESS
Devices can communicate between different networks

📡 Key Features
Site-to-site network communication
Static routing implementation
Simulated secure inter-office connectivity

🚀 Result
Successful communication between two different networks
Routing working correctly between sites

📌 Use Case
Branch office connectivity
Enterprise network communication
