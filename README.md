<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

</head>

<body>

<h2>Enterprise Multi-Site Network Lab</h2>

<img src="https://github.com/user-attachments/assets/14fa6c36-c91e-48ac-a7fa-72b23dba2532" width="100%">

<h3>Highlights</h3>
<ul>
<li>Designed a multi-site hub-and-spoke WAN connecting HQ and branch networks</li>
<li>Implemented inter-VLAN routing using Router-on-a-Stick (802.1Q encapsulation)</li>
<li>Configured centralized DHCP server with IP helper-address (DHCP relay)</li>
<li>Built VLAN-based network segmentation for multiple departments (Sales, IT, HR, Marketing)</li>
<li>Applied static routing to enable end-to-end connectivity across all sites</li>
<li>Implemented Layer 2 security features</li>
<li>Port Security (MAC limiting)</li>
<li>DHCP Snooping (rogue DHCP protection)</li>
<li>Used VTP for centralized VLAN management within the HQ switching domain</li>
<li>Configured trunk links (802.1Q) between switches and router</li>
<li>Applied basic device hardening (enable secret, line passwords, password encryption)</li>
<li>Verified full connectivity with end-to-end ICMP testing across VLANs and sites</li>
</ul>

<h3>Network Architecture</h3>
<ul>
<li>Topology: Hub-and-Spoke WAN</li>
<li>Core Site: Colombo HQ</li>
<li>Branch Sites: Jaffna, Kandy, Galle</li>
<li>WAN Links: /30 subnet addressing for efficient IP usage</li>
<li>LAN Design: Separate subnet per site (192.168.x.0/24)</li>
</ul>

<p>
This design ensures scalability, centralized control, and efficient traffic management.
</p>

<h3>VLAN Segmentation (HQ)</h3>
<ul>
<li>VLAN 10 – Sales</li>
<li>VLAN 20 – IT</li>
<li>VLAN 30 – HR</li>
<li>VLAN 40 – Marketing</li>
<li>VLAN 50 – Server (DHCP)</li>
</ul>

<p>
Each VLAN operates as an independent broadcast domain, improving performance and security.
</p>

<h3>Core Networking Features</h3>

<h4>Inter-VLAN Routing</h4>
<ul>
<li>Implemented using router subinterfaces with 802.1Q encapsulation</li>
<li>Each VLAN assigned a gateway IP</li>
<li>Enables communication between VLANs</li>
</ul>

<h4>Static Routing</h4>
<ul>
<li>Configured network routes across all routers</li>
<li>Ensures end-to-end communication between HQ and branch sites</li>
</ul>

<h4>Centralized DHCP with Relay</h4>
<ul>
<li>DHCP server placed in VLAN 50</li>
<li>Multiple DHCP pools configured for each VLAN</li>
<li>IP helper-address used to forward DHCP requests across networks</li>
</ul>

<h3>Switching and VLAN Management</h3>

<h4>Trunking</h4>
<ul>
<li>Implemented using IEEE 802.1Q between switches and router</li>
<li>Allows multiple VLAN traffic over a single link</li>
</ul>

<h4>VTP</h4>
<ul>
<li>Used for centralized VLAN management within HQ switching domain</li>
<li>Reduces manual VLAN configuration</li>
</ul>

<h3>Security Features</h3>
<ul>
<li>Port Security (MAC limiting)</li>
<li>DHCP Snooping (rogue DHCP protection)</li>
<li>Device hardening with enable secret and password encryption</li>
</ul>

<h3>Testing and Validation</h3>
<ul>
<li>Verified inter-VLAN communication using ICMP</li>
<li>Confirmed DHCP IP allocation across all VLANs and branch sites</li>
<li>Validated WAN connectivity between all locations</li>
<li>Ensured security features function as expected</li>
</ul>


</body>
</html>
