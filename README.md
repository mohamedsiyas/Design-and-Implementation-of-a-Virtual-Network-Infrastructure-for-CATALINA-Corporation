# Design-and-Implementation-of-a-Virtual-Network-Infrastructure-for-CATALINA-Corporation

In the provided network configuration for Catalina Corporation, a star topology is implemented where a centralized router connects four departments: Administration, Finance, Marketing, and IT. Each department has its own subnet with specific IP ranges and configurations. The network design involves the use of VLANs to logically separate the departments, enhancing security and manageability.

Subnet IP Addressing and Configuration:

Administration Department:
Network IP: 192.168.14.0/26
Range: 192.168.14.1 - 192.168.14.62
Subnet Mask: 255.255.255.192
Devices: PCs, printers, and a Human Resource Information System (HRIS) server. Only one PC in Administration can connect to specific PCs in other departments.

Finance Department:
Network IP: 192.168.14.64/26
Range: 192.168.14.65 - 192.168.14.126
Subnet Mask: 255.255.255.192
Devices: PCs, printers, and an Accounting Information System (AIS) server. One PC in Finance can communicate with a PC in other departments.

Marketing Department:
Network IP: 192.168.14.128/26
Range: 192.168.14.129 - 192.168.14.190
Subnet Mask: 255.255.255.192
Devices: PCs, printers, and a Marketing Information System (MKIS) server. One PC in Marketing can communicate with a PC in other departments.

IT Department:
Network IP: 192.168.14.192/26
Range: 192.168.14.193 - 192.168.14.254
Subnet Mask: 255.255.255.192
Devices: PCs, and a Virtual Learning Environment System (VLES) server. One PC in IT can communicate with PCs in other departments.

The centralized router connects each department using specific interface ports with corresponding IP addresses serving as default gateways. The network is secured with ACLs (Access Control Lists) configured on the router, allowing only specific inter-departmental communication between designated PCs while restricting access to other devices.

This network design emphasizes security, with strict ACL rules and dedicated subnets for each department, ensuring controlled communication and enhanced security across the entire organization.

The network configuration for Catalina Corporation is organized using a star topology, where a centralized router serves as the core of the network, connecting four key departments: Administration, Finance, Marketing, and IT. Each department is allocated its own subnet, with specific IP ranges, ensuring that network traffic is segmented and secure.

Centralized Router and Department Connections
The centralized router acts as the network's hub, with four main interface ports connecting to the switches of each department. These interface ports are configured with IP addresses that serve as the default gateways for the devices within their respective departments.

Administration Department:
Connected to the router through interface FastEthernet0/0, assigned the IP address 192.168.14.1.
The subnet allocated to this department is 192.168.14.0/26, with a range of 192.168.14.1 - 192.168.14.62.
Devices include PCs, printers, and a Human Resource Information System (HRIS) server, all configured to use the default gateway 192.168.14.1.

Finance Department:
Linked to the router via interface FastEthernet1/0, with the IP address 192.168.14.65.
The subnet for Finance is 192.168.14.64/26, covering the range 192.168.14.65 - 192.168.14.126.
The department's network includes PCs, printers, and an Accounting Information System (AIS) server, all utilizing 192.168.14.65 as the default gateway.

Marketing Department:
Connected to the router on interface GigabitEthernet6/0, with the IP address 192.168.14.129.
The assigned subnet is 192.168.14.128/26, spanning 192.168.14.129 - 192.168.14.190.
The network configuration includes PCs, printers, and a Marketing Information System (MKIS) server, with the default gateway set to 192.168.14.129.

IT Department:
Connected through interface GigabitEthernet7/0, with the IP address 192.168.14.193.
The subnet allocated is 192.168.14.192/26, covering 192.168.14.193 - 192.168.14.254.
This department includes PCs and a Virtual Learning Environment System (VLES) server, with 192.168.14.193 as the default gateway.
Internet and Cloud Connectivity
The IT department is also responsible for managing internet connectivity for the entire organization. The internet connection is routed through the IT department, which then distributes it to the other departments. The IP address used for the internet connection is 192.168.14.254, ensuring all departments have access to external resources.

Additionally, a cloud server is included in the network, configured with the IP address 100.100.133.1, and connected to the network through interface GigabitEthernet0/2 on the centralized router. This cloud server is accessible to all departments, providing centralized services like DNS and HTTP.

Security and Access Control
The network's security is reinforced with Access Control Lists (ACLs) configured on the centralized router. These ACLs ensure that only specific PCs within each department can communicate with designated PCs in other departments, while all other devices are restricted. For example, a PC in the IT department (IP 192.168.14.220) can only communicate with specified PCs in the Administration, Finance, and Marketing departments, while other communications are blocked.
