🏛️ CENBANK VLAN Infrastructure Project

This project documents and manages the VLAN architecture for CENBANK's enterprise network. It provides a scalable, secure, and modular framework for segmenting network traffic across departments, services, and physical locations. The configuration files and documentation in this repository support centralized routing, dynamic IP allocation, and policy enforcement across the organization.

 🎯 Project Objectives
•	Network Segmentation: Isolate traffic by department and function to enhance security and performance.
•	Centralized Routing: Use core routers to manage inter-VLAN communication and apply access control policies.
•	-Dynamic IP Allocation: Align each VLAN with a DHCP pool to automate IP address assignment.
•	Scalability: Enable easy expansion by adding new VLANs and DHCP pools without disrupting existing services.
•	Documentation & Maintainability: Provide clear, version-controlled configuration files and strategy documents for network engineers.

 🧱 Network Architecture
•	Access Layer: End-user devices connect to access switches.
•	Distribution Layer: VLANs are defined and managed on distribution switches.
•	Core Layer: Core routers handle inter-VLAN routing via trunk links.
•	DHCP Relay: IP helper addresses forward DHCP requests to centralized servers.
•	All VLANs are trunked from distribution switches to core routers using 802.1Q encapsulation. Routing is performed via Switch Virtual Interfaces (SVIs) on the core.

🧭 Use Cases
🔐 Security Isolation
•	Finance VLAN is isolated from Guest VLAN to protect sensitive data.
•	HR VLAN is restricted to authorized personnel only.

🌐 Guest Access
•	Visitors connect to the Guest VLAN, which is firewalled from internal systems.

🏢 Departmental Segmentation
•	Each department (e.g., Accounting, Marketing, Logistics) has its own VLAN and DHCP pool.
•	Enables bandwidth control, traffic shaping, and targeted monitoring.

🖥️ Server Infrastructure
•	A dedicated Server VLAN supports centralized services with a large DHCP pool and static IP reservations.

🛠️ Technologies & Standards
•	Cisco IOS (or compatible CLI syntax)
•	802.1Q VLAN tagging
•	DHCP Relay (IP Helper)
•	Layer 3 Inter-VLAN Routing
•	ACLs and QoS (optional)

 👥 Contributors & Roles
•	Network Engineers: Design and implement VLANs and routing.
•	System Administrators: Manage DHCP servers and DNS.
•	Security Team**: Define ACLs and monitor traffic.
•	IT Support: Troubleshoot VLAN-related issues.

