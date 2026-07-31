# Enterprise Network Design and Implementation Using Cisco Packet Tracer

A professional enterprise network simulation developed in **Cisco Packet Tracer** that demonstrates the design, configuration, and verification of a VLAN-based network using **Router-on-a-Stick (ROAS)** architecture. The project implements centralized network services including **DHCP, DNS, HTTP/HTTPS, FTP, TFTP, NTP, Syslog, and SNMP** to simulate a real-world enterprise environment.

---

## 📌 Project Overview

This project focuses on building a scalable enterprise network with centralized services while minimizing hardware requirements. The network is segmented using VLANs, allowing secure communication between departments through inter-VLAN routing.

A single Enterprise Server provides all required network services, making the design efficient and easy to manage.

---

## 🎯 Objectives

- Design a structured enterprise LAN.
- Implement VLAN segmentation.
- Configure Router-on-a-Stick (ROAS).
- Enable centralized DHCP services.
- Configure DNS for hostname resolution.
- Deploy HTTP and HTTPS web services.
- Configure FTP and TFTP file transfer services.
- Synchronize network devices using NTP.
- Collect logs using Syslog.
- Configure SNMP for network monitoring.
- Verify connectivity and service availability.

---

# 🏗 Network Topology

```
                   +----------------+
                   |     Router R1  |
                   +----------------+
                     G0/0      G0/1
                       |         |
                    Trunk     Server LAN
                       |         |
                +---------------+
                |    SW-Core    |
                +---------------+
                 /             \
                /               \
        +------------+     +------------+
        | SW-Dept A  |     | SW-Dept B  |
        +------------+     +------------+
        |  |  |            |  |  |
      PC1 PC2 PC3       PC4 PC5 PC6

                   |
         +----------------------+
         | Enterprise Server    |
         | DHCP | DNS | HTTP    |
         | HTTPS | FTP | TFTP   |
         | NTP | Syslog | SNMP  |
         +----------------------+
```

---

# 🖥 Devices Used

| Device | Quantity |
|----------|---------:|
| Cisco 2911 Router | 1 |
| Cisco 2960 Core Switch | 1 |
| Cisco 2960 Access Switch | 2 |
| Enterprise Server | 1 |
| PCs | 6 |

**Total Devices:** 11

---

# 🌐 IP Addressing Scheme

| Network | Address |
|----------|------------|
| Server LAN | 192.168.1.0/24 |
| Department A | 192.168.10.0/24 |
| Department B | 192.168.20.0/24 |

### Router Interfaces

| Interface | IP Address |
|------------|------------|
| G0/1 | 192.168.1.1 |
| G0/0.10 | 192.168.10.1 |
| G0/0.20 | 192.168.20.1 |

### Enterprise Server

| Device | IP Address |
|----------|------------|
| Enterprise Server | 192.168.1.10 |

---

# 🛠 Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- VLANs
- Router-on-a-Stick (ROAS)
- DHCP
- DNS
- HTTP
- HTTPS
- FTP
- TFTP
- NTP
- Syslog
- SNMP

---

# ⚙ Configured Services

## ✅ DHCP

- Dynamic IP assignment
- Separate DHCP pools for both VLANs
- Centralized DHCP Server

---

## ✅ DNS

- Hostname resolution
- Custom DNS records

Example:

```
enterprise.local
```

---

## ✅ HTTP & HTTPS

Configured web services for browser access.

```
http://192.168.1.10
```

```
https://192.168.1.10
```

---

## ✅ FTP

Configured FTP server for secure file sharing.

Default account:

```
Username: cisco
Password: cisco
```

---

## ✅ TFTP

Configured TFTP server for router configuration backups.

Example command:

```
copy running-config tftp
```

---

## ✅ NTP

Configured centralized Network Time Protocol server.

Verification:

```
show ntp status
```

---

## ✅ Syslog

Configured centralized log collection.

Example:

```
logging 192.168.1.10
```

---

## ✅ SNMP

Configured network monitoring using community strings.

```
public
private
```

---

# 🔄 Routing

Router-on-a-Stick (ROAS) was implemented using IEEE 802.1Q encapsulation.

Configured VLANs

- VLAN 10 – Department A
- VLAN 20 – Department B

Inter-VLAN routing allows communication between both departments.

---

# 🧪 Verification

The following tests were successfully completed:

- DHCP Lease Verification
- Inter-VLAN Routing
- Server Connectivity
- DNS Resolution
- HTTP Access
- HTTPS Access
- FTP Login
- TFTP Backup
- NTP Synchronization
- Syslog Collection
- SNMP Monitoring

Useful verification commands:

```
show ip interface brief
```

```
show ip route
```

```
show vlan brief
```

```
show interfaces trunk
```

```
show ntp status
```

```
show running-config
```

---

# 📂 Repository Structure

```
Enterprise-Network-Services/
│
├── PacketTracer/
│   └── Enterprise_Network.pkt
│
├── Report/
│   └── Enterprise_Network_Report.pdf
│
├── Screenshots/
│   ├── Topology.png
│   ├── DHCP.png
│   ├── DNS.png
│   ├── HTTP.png
│   ├── FTP.png
│   ├── TFTP.png
│   ├── NTP.png
│   ├── Syslog.png
│   └── SNMP.png
│
└── README.md
```

---

# 📸 Project Screenshots

Add your screenshots here after uploading.

- Network Topology
- DHCP Configuration
- DNS Test
- HTTP Webpage
- HTTPS Webpage
- FTP Login
- TFTP Backup
- NTP Synchronization
- Syslog Logs
- SNMP Configuration

---

# 📚 Learning Outcomes

Through this project, the following networking concepts were implemented and verified:

- Enterprise Network Design
- VLAN Segmentation
- Router-on-a-Stick Configuration
- Layer 2 Switching
- Layer 3 Routing
- Centralized Network Services
- Cisco IOS Configuration
- Network Troubleshooting
- Enterprise Service Deployment
- Network Verification and Testing

---

# 🎓 Academic Purpose

This project was developed as part of a **Networking Security (NETSEC)** laboratory assignment to demonstrate the implementation of enterprise networking concepts using Cisco Packet Tracer.

---

# 👨‍💻 Author

**Muneeb Ahmed**

**Company: ITsimplera**

---

## ⭐ If you found this project helpful, consider giving it a star!
