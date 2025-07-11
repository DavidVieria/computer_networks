# 🌐 Computer Networks: Campus Simulation Project

<br>

```
⚠️ This repository was created as part of the Curricular Unit of "Redes de Computadores (RCOMP)" in the 4th semester of the Bachelor’s Degree in Informatics Engineering at ISEP, and was therefore developed as a group project.
```

## 📝 Project Overview

This project simulates a campus network using Cisco Packet Tracer, modeling a real-world scenario with four interconnected buildings and external Internet access. The network is designed according to best practices in both physical and logical network design, including structured cabling, VLAN segmentation, routing, security policies, and essential network services (DHCP, DNS, VoIP, NAT, Firewall).

The project is organized into three main sprints, each focusing on different OSI layers and network functionalities, progressively building a robust and secure campus network.

---

## 🏗️ Sprint 1 – Physical Analysis & Layer 1 Design

- **Objective:** Analyze and design the physical infrastructure (Layer 1) for each building.
- **Tasks:**
  - Floor plans and device placement for each building.
  - Structured cabling design (copper/fiber), including backbone links.
  - Identification and labeling of network outlets, access points, and main distribution frames.
  - Documentation of physical topology and cabling maps.
- **Outcome:** A detailed physical plan for each building, ensuring scalability and redundancy.

---

## 🧩 Sprint 2 – Logical Analysis: Layer 2 & Initial Layer 3/4

- **Objective:** Develop the logical network, focusing on Layer 2 (switching, VLANs) and initial Layer 3/4 (routing, addressing).
- **Tasks:**
  - Device naming conventions and placement in Packet Tracer.
  - VLAN creation for each building (user, Wi-Fi, DMZ, VoIP, backbone).
  - VTP domain configuration and trunking between switches.
  - Static IPv4 addressing and subnetting for all VLANs.
  - Router-on-a-stick configuration for inter-VLAN routing.
  - Backbone interconnection between buildings.
  - Initial static routing between buildings and backbone.
  - Validation of logical paths and redundancy.
- **Outcome:** Each building operates as a segmented, routed network, interconnected via a campus backbone.

---

## 🚀 Sprint 3 – Advanced Logical Design: Layer 3/4 & Layer 7 (Application Services)

- **Objective:** Finalize and enhance the logical network, introducing advanced Layer 3/4 features and application-level (Layer 7) services.
- **Tasks:**
  - Migration from static to dynamic routing using OSPF with multiple areas (one per building, backbone area 0).
  - Implementation of DHCPv4 for all user VLANs (with option 150 for VoIP).
  - Deployment of VoIP services (Cisco 7960 IP phones, voice VLANs, dial-peers for inter-building calls).
  - DNS architecture: hierarchical domain with authoritative servers in each building (main domain plus subdomains), glue records, and FQDNs for all services.
  - HTTP/HTTPS servers in DMZs, with custom HTML pages identifying each building.
  - Static NAT (port forwarding) for external access to DMZ web/DNS servers.
  - Firewall implementation using ACLs on routers, enforcing security policies (anti-spoofing, DMZ protection, service restrictions, ICMP, etc.).
  - Integration and validation of all services in a unified campus simulation.
- **Outcome:** A fully functional, secure, and service-rich campus network, ready for real-world deployment scenarios, including several Layer 7 (application) services such as DNS, HTTP/HTTPS, and VoIP.
- **Note:** During Sprint 3, we also took the opportunity to review and improve some configurations and design choices made in Sprint 2. Although these were not incorrect, they were refined to better align with best practices and to ensure greater consistency and robustness across the campus network.

---

## 📄 Documentation

- Each sprint folder contains detailed planning, configuration files, and Packet Tracer simulations.
- The `statements` directory includes the official requirements for each sprint.
- All design decisions, addressing plans, VLAN tables, and service configurations are documented in the respective `planning.md` files.

---

## 🛠️ Technologies & Standards

- **Simulation Tool:** Cisco Packet Tracer 8.2.2
- **Network Devices:** Cisco 2811 routers, managed switches, Cisco 7960 IP phones
- **Protocols & Services:** Ethernet, VLAN, VTP, OSPF, DHCP, DNS, NAT, ACLs, VoIP, HTTP/HTTPS
- **Best Practices:** Structured cabling, device naming conventions, hierarchical addressing, security by design

---

## 👥 Team

| Name                     | Building |
|--------------------------|----------|
| Igor Coutinho (1230543)  | 1        |
| David Vieira (1230487)   | 2        |
| Rafael Barbosa (1230544) | 3        |
| Daniel Silva (1231046)   | 4        |

---

> **This project demonstrates a comprehensive approach to campus network design, from physical infrastructure to advanced logical services and security, following real-world standards and best practices.**
