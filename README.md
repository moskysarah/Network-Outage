# Network-Outage 
🧭 Project Overview

Design and configuration of KADEA’s new building network.

Goals:

VLAN-based department isolation

Secure guest Wi-Fi

Inter-VLAN routing for Management

Internet access for all users

🎯 Requirements

20 employees

Accounting: 5

Sales: 10

Management: 3

Guest Wi-Fi: 2 users

Departments isolated

Only Management can access others

Internet for all

Basic guest security

🏗️ Network Architecture

Devices:

Router (2911/1941)

Switch (2960)

Test PCs

WRT300N (guest Wi-Fi)

Design:

Router-on-a-Stick

VLAN segmentation

Trunk between switch and router

🌐 IP Addressing Plan
Service	VLAN	Network	Gateway
Accounting	10	192.168.10.0/24	192.168.10.254
Sales	20	192.168.20.0/24	192.168.20.254
Management	30	192.168.30.0/24	192.168.30.254
Guest Wi-Fi	40	192.168.40.0/24	192.168.40.254
🔧 Switch

VLANs: 10, 20, 30, 40

Access ports assigned

Trunk to router configured

## 🖼️ Network Topology

![Network Topology](images/topology.png)



🚦 Router

Subinterfaces configured

Inter-VLAN routing enabled
