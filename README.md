📡 Inter-VLAN Routing using Router-on-a-Stick (Cisco Packet Tracer)
📘 Project Overview

This project demonstrates the configuration of VLANs and inter-VLAN routing using the router-on-a-stick method in Cisco Packet Tracer.
Two separate networks (HR and SALES) are segmented using VLANs and connected through a single router interface configured with subinterfaces.

The goal of this project is to show practical understanding of:

VLAN segmentation

Trunking

Router subinterfaces

Inter-VLAN communication


🧩 Network Topology

Devices Used and connections used:

1 × Cisco Router (1941)

1 × Cisco Switch (2960)

4 × PCs

Copper Straight-Through


VLAN Design:

| VLAN | Name  | Network         | Gateway      |
| ---- | ----- | --------------- | ------------ |
| 10   | HR    | 192.168.10.0/24 | 192.168.10.1 |
| 20   | SALES | 192.168.20.0/24 | 192.168.20.1 |



🖥️ IP Addressing
HR VLAN (10)

PC1: 192.168.10.2 /24

PC2: 192.168.10.3 /24

Gateway: 192.168.10.1

SALES VLAN (20)

PC3: 192.168.20.2 /24

PC4: 192.168.20.3 /24

Gateway: 192.168.20.1


⚙️ Configuration Summary
Switch Configuration

Created VLAN 10 (HR) and VLAN 20 (SALES)

Assigned access ports:

Fa0/1–Fa0/2 → VLAN 10

Fa0/3–Fa0/4 → VLAN 20

Configured trunk port to router on G0/1

Router Configuration

Configured router-on-a-stick using subinterfaces:

G0/0.10 → VLAN 10

G0/0.20 → VLAN 20

Enabled 802.1Q encapsulation

Assigned default gateway IPs


✅ Verification & Testing

Connectivity was verified using ICMP ping tests:

HR → HR communication ✔

SALES → SALES communication ✔

HR → SALES communication ✔

SALES → HR communication ✔

Key verification commands:

show vlan brief
show interfaces trunk
show ip interface brief
ping




🧠 Skills Demonstrated

VLAN configuration

Trunking (802.1Q)

Router-on-a-stick inter-VLAN routing

IP addressing and subnetting

Network troubleshooting and verification

Cisco IOS CLI usage


📂 Files Included

.pkt topology file

Screenshots of:

Network topology

IP configurations

VLAN configuration

Trunk configuration

Router subinterfaces

Successful ping tests




🚀 Future Improvements

Add DHCP for automatic IP assignment per VLAN

Implement ACLs to control inter-VLAN traffic

Expand topology with multiple switches

Add NAT and internet connectivity



🏁 Conclusion

This project demonstrates a fundamental enterprise networking concept: segmentation with VLANs and routing between them using a single router interface.
It reflects real-world small business network design and aligns with CCNA / Network+ networking principles.
