1. Introduction & Project Overview
This project demonstrates the design and simulation of a secure, scalable Wide Area Network (WAN) connecting 5 distinct School Campuses located in different geographical areas. The primary objective is to establish seamless communication between campuses while maintaining strict operational security through network segmentation.

Key Objectives:

Inter-Campus Connectivity: Connecting 5 geographically separated schools using Serial and Fiber optic connections.

Departmental Segmentation: Segregating traffic between the Head Office (VLAN 10) and the Campus Office (VLAN 20) using Virtual LANs.

Dynamic IP Management: Implementing automated IP allocation via DHCP for all staff and administrative devices.

Centralized Services: Configuring dedicated Mail and DNS Servers to facilitate official internal communication.

Optimized Routing: Ensuring end-to-end connectivity using Dynamic Routing Protocols (OSPF/RIP).
2. Network Topology & Hardware
The infrastructure utilizes a Star/Mesh Topology to ensure high availability and redundancy.

Cisco Routers: Employed for efficient Inter-Campus routing.

Multilayer Switches: Used for high-speed Inter-VLAN routing within each school campus.

Centralized Servers: Hosting critical services including DHCP, DNS, and SMTP/POP3 Email.

End Devices: A mix of PCs and Laptops assigned to Principal offices, Faculty, and Administrative staff.
3. IP Addressing Scheme (Campus Breakdown)School CampusNetwork AddressHead Office (VLAN 10)Campus Office (VLAN 20)Server IPCampus 1 (Main)192.168.10.0.10.x.20.x (Segregated)192.168.10.200Campus 2192.168.30.0.30.x.40.x192.168.30.200Campus 3192.168.50.0.50.x.60.x192.168.50.200Campus 4192.168.70.0.70.x.80.x192.168.70.200Campus 5192.168.90.0.90.x.100.x192.168.90.200
4. Configuration Details
4.1 VLAN Segmentation
To ensure administrative privacy and security, two specific VLANs were created in each campus:

VLAN 10 (Head Office): Reserved for Management and Principals. This VLAN has high-priority access to the Mail Servers and cross-campus resources.

VLAN 20 (Campus Office): Designated for teachers and general staff. Traffic in this VLAN is restricted to prevent unauthorized access to sensitive management data.

4.2 DHCP & DNS Services
DHCP: Configured on the core routers to automatically assign IP addresses, Default Gateways, and DNS details to all workstations.

DNS: An A-Record based system was established to resolve local domains such as campus1.edu and headquarters.edu.

4.3 Professional Email Setup
SMTP and POP3 services were enabled, allowing staff (e.g., principal@campus1.edu) to send and receive official correspondence across the entire school network successfully.
5. Security & Verification
Access Control Lists (ACLs): Extended ACLs were implemented on edge routers. These policies successfully block the Campus Office (VLAN 20) from accessing sensitive Head Office segments while allowing the Head Office to monitor the entire network.

Connectivity Testing: Verified via Ping Tests (confirming end-to-end reachability) and Email Simulations (confirming application-layer success).
6. Conclusion
This project successfully simulates a robust and modern network for an educational organization. By utilizing professional-grade configurations like VLANs, OSPF, and ACLs, the network provides a secure environment for school data while ensuring all five campuses remain connected. The system is reliable, scalable, and meets all technical requirements for a professional school management infrastructure.
<img width="865" height="647" alt="image" src="https://github.com/user-attachments/assets/49386bb0-142e-4585-a7df-185442f9f11f" />

