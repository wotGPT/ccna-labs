# CCNA Lab Portfolio

This repository contains hands-on labs completed while studying for the CCNA certification. Each lab demonstrates practical networking skills, structured troubleshooting, and an understanding of core networking concepts required for entry-level networking and NOC positions.

---

## Labs

### Lab-01-Basic-Network

- Built a simple LAN using a switch and verified connectivity between two PCs
- Practiced IPv4 addressing and basic network communication
- Introduced troubleshooting using ping

### Lab-01.5-Mini-ARP

- Explored ARP packet behavior
- Observed IP-to-MAC address resolution
- Used Packet Tracer Simulation Mode to analyze ARP traffic

### Lab-02-OSI-Model-&-Packet-Flow

- Examined packet flow through the OSI model
- Observed ARP and ICMP traffic
- Reinforced encapsulation and decapsulation concepts

### Lab-03-Subnetting-&-Inter-Network-Communication

- Connected multiple networks using a router
- Configured router interfaces and default gateways
- Practiced Layer 3 forwarding between networks

### Lab-04-Static-Routing

- Built a two-router network
- Configured static routes
- Verified communication across remote networks
- Examined routing table entries learned through static routing

### Lab-05-Dynamic-Routing-(OSPF)

- Implemented OSPF dynamic routing
- Established OSPF neighbor relationships
- Replaced static routes with automated route learning
- Verified OSPF-learned routes in the routing table

### Lab-06-Multi-Router-OSPF

- Expanded OSPF into a three-router topology
- Configured multiple OSPF neighbor relationships
- Used /30 point-to-point WAN networks
- Verified route propagation across multiple routers
- Reinforced OSPF Area 0 concepts

### Lab-07-OSPF-Failover-&-Convergence

- Simulated a WAN link failure between routers
- Observed OSPF neighbor changes during convergence
- Verified automatic route recalculation
- Confirmed end-to-end connectivity through an alternate path
- Restored the failed WAN link and verified OSPF recovery
- Demonstrated network resiliency using dynamic routing

### Lab-08-VLAN-Fundamentals

- Created VLAN 10 (SALES) and VLAN 20 (ACCOUNTING)
- Assigned switch access ports to specific VLANs
- Verified VLAN membership using switch commands
- Demonstrated network segmentation using VLANs
- Tested communication between VLANs
- Observed how VLANs create separate broadcast domains

### Lab-09-VLAN-Trunking

- Configured VLANs across multiple switches
- Created an 802.1Q trunk connection
- Verified trunk operation using switch commands
- Demonstrated VLAN traffic traversing between switches
- Tested communication before and after trunk configuration
- Reinforced the relationship between access ports and trunk ports

### Lab-10-Inter-VLAN-Routing

- Implemented Router-on-a-Stick
- Configured 802.1Q trunking between a switch and router
- Created router subinterfaces for multiple VLANs
- Configured default gateways for VLAN networks
- Verified communication between VLAN 10 and VLAN 20
- Demonstrated Layer 3 routing between VLANs

### Lab-11-Spanning-Tree-Protocol

- Configured redundant switch connections
- Observed STP Root Bridge election
- Identified blocked ports used to prevent Layer 2 loops
- Simulated a switch-link failure
- Verified STP convergence and backup path activation
- Demonstrated Layer 2 redundancy and fault tolerance

### Lab-12-EtherChannel

- Configured EtherChannel using LACP
- Bundled multiple physical links into a logical connection
- Verified EtherChannel operation using switch commands
- Observed STP interaction with EtherChannel
- Simulated a member-link failure
- Demonstrated increased redundancy and bandwidth utilization

### Lab-13-DHCP

- Configured a Cisco router as a DHCP server
- Created and managed a DHCP address pool
- Reserved addresses using DHCP exclusions
- Automatically assigned IP configuration to a client
- Verified DHCP leases using router commands
- Demonstrated automated network configuration services

### Lab-14-NAT

- Configured NAT overload (PAT)
- Defined NAT inside and outside interfaces
- Created translation rules using access lists
- Verified private-to-public address translation
- Connected a private LAN to a simulated public network
- Examined NAT translation tables
- Demonstrated how Internet connectivity is enabled through NAT

### Lab-15-Standard-ACLs

- Configured Standard Access Control Lists
- Filtered traffic based on source IP addresses
- Applied ACLs to router interfaces
- Verified ACL operation using hit counters
- Demonstrated traffic blocking and restoration
- Introduced network traffic control and security concepts

### Lab-16-Extended-ACLs

- Configured Extended Access Control Lists
- Filtered traffic using protocols and port numbers
- Blocked HTTP traffic while permitting ICMP traffic
- Applied ACLs to router interfaces
- Verified ACL operation using hit counters
- Demonstrated granular traffic filtering and access control

### Lab-17-IPv6-Fundamentals

- Configured IPv6 addressing on routers and hosts
- Enabled IPv6 routing
- Verified IPv6 interface configuration
- Tested end-to-end IPv6 connectivity
- Examined Neighbor Discovery Protocol (NDP)
- Verified IPv6 routing table entries
- Introduced IPv6 addressing fundamentals

### Lab-18-IPv6-Static-Routing

- Configured IPv6 addressing across multiple routers
- Enabled IPv6 routing on Cisco routers
- Built an IPv6 point-to-point WAN
- Configured IPv6 static routes
- Verified IPv6 routing tables
- Tested end-to-end IPv6 communication between remote LANs
- Reinforced IPv6 routing concepts using static routes

---

## Tools Used

- Cisco Packet Tracer
- GitHub
- Markdown Documentation

---

## Skills Demonstrated

- IPv4 Addressing
- IPv6 Addressing
- IPv6 Static Routing
- Neighbor Discovery Protocol (NDP)
- Subnetting Fundamentals
- ARP Analysis
- Router Configuration
- Static Routing
- Dynamic Routing (OSPF)
- VLAN Configuration
- VLAN Trunking
- Inter-VLAN Routing
- Spanning Tree Protocol (STP)
- EtherChannel (LACP)
- DHCP Configuration
- Network Address Translation (NAT/PAT)
- Standard Access Control Lists (ACLs)
- Extended Access Control Lists (ACLs)
- Layer 2 Redundancy
- Network Failover
- Network Segmentation
- Route Verification
- Network Troubleshooting
- Network Documentation
- GitHub Portfolio Management

---

## Goal

To develop practical networking skills, build a professional GitHub portfolio, and prepare for the CCNA certification while working toward an entry-level NOC or networking position.

---

## Notes

- Each lab includes screenshots, configuration verification, and documented results.
- Labs are designed to build progressively from networking fundamentals to enterprise routing, switching, IPv6, security, services, and troubleshooting.
- All labs are created and documented using Cisco Packet Tracer and GitHub.
