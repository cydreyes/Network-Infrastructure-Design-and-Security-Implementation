### Devices
___
- 4 PCs
- 3 Cisco 2960 Switches
- 3 Cisco 2911 Routers

### Logical Design
___

### Router A:
- GigabitEthernet0/0 connects to Switch A on port 
FastEthernet0/2

### Switch A: 
- Port FastEthernet0/1 connects to PC-A on port 
FastEthernet0.0
- Port FastEthernet0/3 connects to PC-B 
on port FastEthernet0

### Router B:
- GigabitEthernet0/1 connects to Switch B on port 
FastEthernet0/1

### Switch B:
-  Port FastEthernet0/3 connects to PC-C on port 
FastEthernet0

### Router C:
- Serial0/0/0 connects to the internet
- GigabitEthernet0/0 connects to Switch C on port 
FastEthernet0/3

### Switch C: 
- Port FastEthernet0/1 connects to Router A on 
GigabitEthernet0/1. 
- Port FastEthernet0/2 connects to Router B on 
GigabitEthernet0/0.

### Configurations

___

### OSPF (Open Shortest Path First):
- Implemented across all three routers to enable dynamic routing
- Ensures load balancing and redundancy by providing multiple paths between branches

### NAT (Network Address Translation):
- Configured to allow routers to share a single public IP address
- Enhances security by masking internal IP addresses from external networks

### ACL (Access Control List):
- Mitigates unauthorized access by filtering incoming traffic
- Helps control traffic flow by allowing or denying certain traffic
- Router A: ACLs to 
permit traffic from 
subnet 
192.168.0.0/24
- Router B: ACLs to 
permit traffic from 
subnet 
192.168.0.128/25
- Router C: 
Comprehensive ACLs 
for overall network 
security

### SSH Access:
- Ensure secure management access through user authentication and encryption

### Test 1: Connectivity Validation
___
### Objective: 
Ensure all devices can communicate with each other, verifying proper network connectivity.

### Procedure: 
- From PC-A, ping PC-B, PC-C, and PC-D.
- From PC-C, ping PC-A, PC-B, and PC-D.
- Analyze the ping responses to confirm successful communication.

### Expected Outcome:
- All devices should return successful ping responses, confirming proper network connectivity and functionality.

### Scalability and Future Expansion
___
### Scalable VLANs
- Enables logical network segmentation for improved traffic management and security.
- Supports seamless expansion as new departments or devices are added.
### Modular Switches
- Designed for scalability, allowing easy addition of new ports to accommodate growth.
### Additional Routers and Switches
- New network devices can be seamlessly integrated into the existing OSPF topology.
- Enhances fault tolerance and overall network resilience.
### IPv6 Implementation
- Ensures future compatibility and readiness for IPv6 adoption.
- Mitigates the risk of IP address exhaustion, supporting long-term network sustainability.



