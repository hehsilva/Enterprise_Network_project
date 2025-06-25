# 🏥 Enterprise Networking Project  –  Health Care Center

## 📘 Project Overview

This project presents a **comprehensive enterprise network design and implementation** for *Health Care Center*, a healthcare provider in Sri Lanka with two locations: **Headquarters** and a **Branch Hospital**, located 20km apart. The solution replaces third-party IT support with an in-house infrastructure ensuring **scalability**, **security**, and **cost-effectiveness** while maintaining **Confidentiality, Integrity, and Availability (CIA)**.

---

## 🧩 Project Objectives

- Design a scalable and secure network using **Cisco Packet Tracer**
- Implement VLAN segmentation, DHCP, DNS, OSPF routing, and secure communication via **VPN and ACL**
- Enable **redundancy, remote access (SSH)**, **port security**, and **PAT/NAT configuration**
- Ensure secure and efficient **inter-department communication** and **internet access**

---

## 🖥️ Network Topology



![Network Topology Screenshot](https://github.com/hehsilva/Enterprise_Network_project/blob/e1148331dc16441f5b4c107feb16ecc9c59f5492/Network%20Topology.jpg)

---

## 🏢 Departments & IP Addressing

**Headquarters Departments (≈60 Users Each):**
- Medical Lead Operation & Consultancy Services (MLOCS)
- Medical Emergency and Reporting (MER)
- Medical Records Management (MRM)
- Information Technology (IT)
- Customer Service (CS)
- Guest/Waiting Area (GWA)

**Branch Departments (≈30 Users Each):**
- Nurses & Surgery Operations (NSO)
- Hospital Labs (HL)
- Human Resources (HR)
- Marketing (MK)
- Finance (FIN)
- Guest/Waiting Area (GWA)

> Base Network: `192.168.100.0/24`  
> Each department assigned a **unique subnet and VLAN**

---

## ⚙️ Technologies Used

- Cisco Packet Tracer
- VLAN & Inter-VLAN Routing
- OSPF Routing Protocol
- Access Control Lists (ACL)
- Port Address Translation (PAT)
- Site-to-Site VPN (IPSec)
- Dynamic Host Configuration Protocol (DHCP)
- Domain Name System (DNS)
- Secure Shell (SSH)
- Wireless Access Points
- Port Security

---

## 🔧 Configuration Steps

Below is the summary of configuration tasks performed in this project:

1. **Network Design and Beautification**  
   - Logical and physical layout design using Cisco Packet Tracer.

2. **Basic Device Settings + SSH Configuration**  
   - Set hostnames, passwords, banner messages.  
   - Enabled SSH on all routers and 13 multilayer switches.

3. **VLAN Creation & Trunking**  
   - Assigned VLANs to each department.  
   - Configured trunk/access ports on switches 12 and 13.

4. **Port Security for Server Site**  
   - Enabled sticky MAC address and violation mode as shutdown.

5. **Subnetting & IP Address Allocation**  
   - Subnetted `192.168.100.0/24` based on department size.  
   - Assigned static IPs to servers, dynamic via DHCP for users.

6. **OSPF Configuration**  
   - Implemented OSPF on routers and switches for route advertisement.

7. **Static IP for Server Room Devices**  
   - Assigned IPs manually to DNS, DHCP, Web, and Email servers.

8. **DHCP Server Setup**  
   - Configured DHCP scopes and excluded ranges on server device.

9. **Inter-VLAN Routing & DHCP Relay**  
   - Configured routing on Layer 3 switches.  
   - Added `ip helper-address` for each VLAN.

10. **Wireless Configuration**  
    - Deployed WAPs in all departments with security settings.

11. **Site-to-Site VPN (IPSec)**  
    - Configured secure tunnel between HQ and Branch routers.

12. **Default Static Routing**  
    - Added default routes on routers and L3 switches using next-hop.

13. **PAT and ACL Configuration**  
    - Configured NAT Overload on edge routers.  
    - Applied extended ACLs to filter traffic.

14. **Testing and Validation**  
    - Verified inter-VLAN, internet, VPN, and ACL functionality using `ping`, `traceroute`, and `show` commands.

---

## 📸 Screenshots

| Description                         | Screenshot |
|-------------------------------------|------------|
| Network Topology Overview           | ![topo](https://github.com/hehsilva/Enterprise_Network_project/blob/e1148331dc16441f5b4c107feb16ecc9c59f5492/Network%20Topology.jpg) |
| VLAN Configuration on Switch        | ![vlan](https://github.com/hehsilva/Enterprise_Network_project/blob/3e0c196408d199a62c13bc4a44ca45fba8ef1035/Images/vlan.jpg) |
| DHCP Server Settings                | ![dhcp](https://github.com/hehsilva/Enterprise_Network_project/blob/ffa9c6b0bc78207496c171c15e9b873f43b824da/Images/dhcp.jpg) |
| VPN Tunnel Established              | ![vpn](https://github.com/hehsilva/Enterprise_Network_project/blob/4169ee9a266ad5abf2eb918f695939ce01778b72/Images/vpn.jpg) |
| OSPF Routing Table                  | ![ospf](screenshots/ospf_routing.png) |
| PAT/NAT Configuration               | ![nat](screenshots/pat_config.png) |
| ACL Applied on Router               | ![acl](screenshots/acl_config.png) |



---

## 👨‍💼 Contributors

- **Hasini Erandi** – Gruop Leader   
- *Janani Chamodya - Gruop member*

---

## 🔒 License

This project is for **educational purposes only**. You may reuse configurations or structure under the [MIT License](LICENSE).

---

## 🛠 Future Improvements

- Add external DNS resolution using simulated Internet servers
- Implement failover using HSRP or VRRP
- Introduce AAA server for centralized authentication

---

## 🧪 Testing & Validation

✔ All departments can communicate via inter-VLAN routing  
✔ HQ and Branch securely communicate using VPN tunnel  
✔ DHCP assigns IPs correctly, servers use static IPs  
✔ Access control via ACLs works as expected  
✔ Internet access working through PAT




