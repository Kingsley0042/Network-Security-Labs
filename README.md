\# Securing a Small Business Network with VLANs and ACLs

\## Overview This Packet Tracer project simulates a small business
network with two departments (Sales and IT), segmented using VLANs,
secured with ACLs, and hardened for management access.

\## Topology - \*\*Devices\*\*: 1 Router (2911), 1 Switch (2960), 4 PCs,
1 Server. - \*\*VLANs\*\*: VLAN 10 (Sales, 192.168.10.0/24), VLAN 20
(IT, 192.168.20.0/24). - \*\*Connections\*\*: Switch trunk to Router
(Fa0/24 to Gig0/0), PCs/Server on access ports.

\## Features - \*\*VLAN Segmentation\*\*: Sales (PC1, PC2) on VLAN 10,
IT (PC3, PC4, Server) on VLAN 20. - \*\*Inter-VLAN Routing\*\*:
Router-on-a-Stick with subinterfaces (Gig0/0.10, Gig0/0.20). -
\*\*ACL\*\*: Sales can only access Server via HTTP (port 80), Telnet to
Router blocked. - \*\*Hardening\*\*: SSH enabled, Telnet disabled,
encrypted passwords.

\## Files - \`secure-network.pkt\`: Packet Tracer project file. -
\`router-config.txt\`: Router configuration. - \`switch-config.txt\`:
Switch configuration. - \`topology.png\`: Network diagram.

\## How to Test 1. Open \`secure-network.pkt\` in Packet Tracer. 2. Ping
within VLANs (e.g., PC1 to PC2). 3. Test inter-VLAN routing (e.g., PC1
to PC3). 4. From Sales: HTTP to Server (192.168.20.50) works, Telnet
fails. 5. SSH to Router (192.168.20.1) or Switch (192.168.20.2) with
\`admin\`/\`admin123\`.
