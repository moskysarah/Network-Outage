# Network-Outage 


🧭 Project Overview

This project consists of designing and configuring the network infrastructure for KADEA’s new building.

The objective is to ensure:

Department isolation using VLANs

Secure guest Wi-Fi

Inter-VLAN routing for the Direction

Internet access for all users

🎯 Requirements

20 employees divided into:

Accounting: 5

Sales: 10

Management: 3

Guest Wi-Fi: 2 simultaneous users

Departments must not communicate with each other

Only Management can access other departments

Internet access for all

Basic security for guest network

🏗️ Network Architecture

Devices used:

Router (2911/1941)

Switch (2960)

PCs for testing

WRT300N for guest Wi-Fi

Design choice:

Router-on-a-Stick for inter-VLAN routing

VLAN segmentation for security

Trunk link between switch and router

🌐 IP Addressing Plan
Service	VLAN	Network	Gateway	DHCP Range
Accounting	10	192.168.10.0/24	192.168.10.254	.10–.200
Sales	20	192.168.20.0/24	192.168.20.254	.10–.200
Management	30	192.168.30.0/24	192.168.30.254	.10–.200
Guest Wi-Fi	40	192.168.40.0/24	192.168.40.254	.10–.200
🔧 Switch Configuration (Summary)

VLANs created: 10, 20, 30, 40

Access ports assigned per department

Trunk configured on uplink port to router

🚦 Router Configuration (Summary)

Subinterfaces configured:

G0/0.10

G0/0.20

G0/0.30

G0/0.40

Inter-VLAN routing enabled

Gateways configured for each VLAN

🧪 Tests Performed

Same VLAN ping ✅

Different VLAN ping ❌

Management → other VLANs ✅

Guest Wi-Fi isolation ✅

Internet connectivity ✅

⚠️ Issues Encountered

Example (à adapter) :

Trunk not working initially

Wrong VLAN assignment on some ports

Subinterfaces were administratively down
