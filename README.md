# VLAN-Based Traffic Segmentation

Design and implementation of VLAN-based traffic segmentation with deterministic multi-router path control using Cisco Packet Tracer.


## Project Overview

<img width="669" height="249" alt="image" src="https://github.com/user-attachments/assets/fe0f5c69-f328-47b8-ad07-a51702bb83d9" />

The initial objective of this project was to separate different data types and route them through distinct network paths.

Since Cisco Packet Tracer does not support Layer 7 (application-level) traffic classification or deep packet inspection, content-based routing could not be implemented directly.  

Therefore, the design was adapted to use VLAN-based logical segmentation and subnet-level routing to simulate controlled traffic separation at Layer 2 and Layer 3.


## Network Architecture

The network is designed to enforce deterministic path control through VLAN-based subnet segmentation:

- **VLAN 10 – 192.168.10.0/24 → Router 0**
- **VLAN 20 – 192.168.20.0/24 → Router 1**
- **Router 2 → Aggregation router**
- Static routing used for fixed path selection

Each VLAN is mapped to a dedicated subnet to ensure logical isolation and predictable Layer 3 forwarding.


## Implementation

- VLAN segmentation configured on the switch  
- Static routes manually defined on all routers  
- Packet flow verified in Simulation Mode  
- Layer 2 forwarding validated via MAC table inspection  

Traffic forwarding behavior:

- VLAN 10 traffic → Router 0  
- VLAN 20 traffic → Router 1  


## Limitations

Due to Cisco Packet Tracer constraints:

- No Layer 7 inspection  
- No application-aware routing  
- No Policy-Based Routing (PBR)  

Traffic engineering is therefore subnet-based rather than content-based.


## Future Improvements

- Policy-Based Routing (PBR)  
- Application-aware routing using GNS3  
- Firewall-integrated routing policies  


## Technical Scope

- VLAN segmentation  
- Static routing  
- Deterministic multi-router design  
- Asymmetric routing analysis  
- Layer 2–Layer 3 interaction  


## Author

Eslemnur Basınlı  
Electronics Engineering Student
