# Project 001: Scalable Small Enterprise Network Design & Implementation

## Project Overview

This project is a small enterprise network designed and built using Cisco Packet Tracer. The network connects different departments, servers, and network devices in one reliable and secure environment.

The design uses two internet service providers to provide internet connectivity and backup in case the primary connection fails. It also uses two distribution switches to improve network availability and reduce downtime.

The project includes VLANs, inter-VLAN routing, OSPF, HSRP, DHCP, DNS, NAT/PAT, and basic network security. The network is designed to support the current needs of a small organization while allowing room for future growth.

This project demonstrates my practical networking skills, network design knowledge, configuration, troubleshooting, and verification.

## Project Goals

The main goals of this project are:

- Connect different departments in one network.
- Separate departments using VLANs.
- Allow devices in different VLANs to communicate where required.
- Provide internet access through two ISPs.
- Use ISP1 as the primary connection and ISP2 as backup.
- Improve network reliability using two distribution switches.
- Provide network services such as DHCP and DNS.
- Protect the network using basic security features.
- Make the network easy to expand as the organization grows.

## Project Ownership

This is my own independent networking project, designed and built by me using Cisco Packet Tracer. It is different from the guided CCNA labs in this repository, where I followed lessons and instructions to practise networking concepts. For this project, I made my own design decisions, built the network, configured the devices, tested the connectivity, and worked through the challenges independently.

## Network Topology and Devices

The network is built using a hierarchical design with edge routers, distribution switches, and access switches.

The topology includes:

- **Two ISPs:** ISP1 is the primary internet connection, while ISP2 provides backup.
- **Two edge routers:** R1 connects to ISP1, and R2 connects to ISP2. Both routers connect to the two distribution switches.
- **Two distribution switches:** DSW1 and DSW2 provide inter-VLAN routing and help improve network availability.
- **Four access switches:** ASW1, ASW2, ASW3, and ASW4 connect end devices to the network.
- **Servers:** A DHCP server provides IP addresses to clients, while a DNS server provides name resolution.
- **End devices:** PCs, printers, and wireless access points are connected through the access switches.

The access switches have uplinks to both distribution switches. This provides an alternative path if one distribution switch or uplink becomes unavailable.

The network uses VLANs to separate departments and network services. Routing between VLANs is handled by the distribution switches.

The topology is designed to provide reliable connectivity, support the current needs of a small organization, and allow future expansion.

## Network Topology

![Project 001 Network Topology](./project001-network-topology.png)

## VLANs and IP Addressing

The network uses VLANs to logically separate departments, servers, and management traffic. Each VLAN has its own IP subnet and default gateway.

| VLAN | Name | Network | Default Gateway |
|---|---|---|---|
| 10 | Administration | 172.16.4.0/25 | 172.16.4.1 |
| 20 | Finance | 172.16.5.128/26 | 172.16.5.129 |
| 30 | Operations | 172.16.4.128/25 | 172.16.4.129 |
| 40 | Guest Wi-Fi | 172.16.5.0/25 | 172.16.5.1 |
| 50 | IT | 172.16.5.192/26 | 172.16.5.193 |
| 60 | Servers | 172.16.6.0/27 | 172.16.6.1 |
| 70 | Management | 172.16.6.32/27 | 172.16.6.33 |
| 999 | Parking VLAN | No IP address | N/A |
