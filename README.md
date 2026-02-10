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

4. IP Addressing Scheme (Campus Breakdown)School CampusNetwork AddressHead Office (VLAN 10)Campus Office (VLAN 20)Server IPCampus 1 (Main)192.168.10.0.10.x.20.x (Segregated)192.168.10.200Campus 2192.168.30.0.30.x.40.x192.168.30.200Campus 3192.168.50.0.50.x.60.x192.168.50.200Campus 4192.168.70.0.70.x.80.x192.168.70.200Campus 5192.168.90.0.90.x.100.x192.168.90.200
   
5. Configuration Details
5.1 VLAN Segmentation
To ensure administrative privacy and security, two specific VLANs were created in each campus:
VLAN 10 (Head Office): Reserved for Management and Principals. This VLAN has high-priority access to the Mail Servers and cross-campus resources.
VLAN 20 (Campus Office): Designated for teachers and general staff. Traffic in this VLAN is restricted to prevent unauthorized access to sensitive management data.
5.2 DHCP & DNS Services
DHCP: Configured on the core routers to automatically assign IP addresses, Default Gateways, and DNS details to all workstations.
DNS: An A-Record based system was established to resolve local domains such as campus1.edu and headquarters.edu.
5.3 Professional Email Setup
SMTP and POP3 services were enabled, allowing staff (e.g., principal@campus1.edu) to send and receive official correspondence across the entire school network successfully.

6. Security & Verification
Access Control Lists (ACLs): Extended ACLs were implemented on edge routers. These policies successfully block the Campus Office (VLAN 20) from accessing sensitive Head Office segments while allowing the Head Office to monitor the entire network.


Connectivity Testing: Verified via Ping Tests (confirming end-to-end reachability) and Email Simulations (confirming application-layer success).
<img width="865" height="647" alt="image" src="https://github.com/user-attachments/assets/49386bb0-142e-4585-a7df-185442f9f11f" />
<img width="865" height="362" alt="image" src="https://github.com/user-attachments/assets/b8eb71c2-aecb-4cc0-9c82-7d2fdc8061e3" />
<img width="865" height="367" alt="image" src="https://github.com/user-attachments/assets/600d7d62-ce64-48e4-8cf9-da4f33d99205" />

EMAIL TEST
<img width="940" height="989" alt="image" src="https://github.com/user-attachments/assets/63473c46-7e32-4ff7-ae8e-ea8f08bf56c8" />
<img width="940" height="257" alt="image" src="https://github.com/user-attachments/assets/4da1e45a-2a21-43e3-96d6-d75f14f64314" />

DHCP OF ALL Campuses
<img width="940" height="967" alt="image" src="https://github.com/user-attachments/assets/b5294cb1-8620-4b5b-a920-620dcdfe6ca4" />
<img width="940" height="992" alt="image" src="https://github.com/user-attachments/assets/690f4043-4e0f-43b5-b065-69fbeb878709" />
<img width="940" height="985" alt="image" src="https://github.com/user-attachments/assets/1e405b99-21ad-4ab8-bfc6-95f447707c55" />
<img width="940" height="975" alt="image" src="https://github.com/user-attachments/assets/8dbd45ec-4f30-40b8-86f0-6cd8bd2d3ee3" />
<img width="940" height="975" alt="image" src="https://github.com/user-attachments/assets/86b7c695-22fc-4277-b5fc-d5b618931143" />
ROUTING TABLE 
<img width="940" height="1031" alt="image" src="https://github.com/user-attachments/assets/350fa407-86f7-4b5e-afad-213d7148135a" />
<img width="940" height="996" alt="image" src="https://github.com/user-attachments/assets/2888ad75-1da5-415e-868b-334823b22b43" />
<img width="940" height="1020" alt="image" src="https://github.com/user-attachments/assets/91d5cecc-a3ae-4d7f-8375-5c1cba94e135" />
<img width="940" height="1001" alt="image" src="https://github.com/user-attachments/assets/c3190442-2d99-4ef1-8365-068ca604af36" />
<img width="940" height="982" alt="image" src="https://github.com/user-attachments/assets/8eb452e8-b073-4bbc-bf66-d4d30ab8c55d" />

ACL
<img width="865" height="169" alt="image" src="https://github.com/user-attachments/assets/73affad0-d078-48be-9146-ee3997aeabb2" />
<img width="865" height="201" alt="image" src="https://github.com/user-attachments/assets/746530ad-c3a4-4c3f-815c-d6a24cbc56c9" />
<img width="865" height="195" alt="image" src="https://github.com/user-attachments/assets/4fbbbe73-21c0-41b1-aa14-89a878aa206c" />
<img width="865" height="190" alt="image" src="https://github.com/user-attachments/assets/0e1e7e80-1236-4293-87a3-e0346e5795d7" />

Security Test (Block Proof of analyst)
<img width="865" height="586" alt="image" src="https://github.com/user-attachments/assets/9988c6f4-5c67-4217-95d7-08136a08baeb" />

Interface Stats
<img width="865" height="911" alt="image" src="https://github.com/user-attachments/assets/12dda88e-a9a8-426a-bdf5-50584f910978" />

Routing Protocol Details
<img width="865" height="911" alt="image" src="https://github.com/user-attachments/assets/dcaef6a4-bf2a-4a09-ac7c-7736c359961d" />

6. Conclusion
This project successfully simulates a robust and modern network for an educational organization. By utilizing professional-grade configurations like VLANs, OSPF, and ACLs, the network provides a secure environment for school data while ensuring all five campuses remain connected. The system is reliable, scalable, and meets all technical requirements for a professional school management infrastructure.
