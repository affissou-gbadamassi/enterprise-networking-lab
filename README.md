# Enterprise Networking Lab

## Project Overview

This project demonstrates the design, configuration, and validation of a simulated enterprise network using Cisco Packet Tracer. The network connects a Headquarters (HQ) and Branch location and implements VLAN segmentation, inter-VLAN routing, DHCP, secure wireless connectivity, voice VLANs, WAN routing, firewall security, and simulated Internet access.

The lab was built to demonstrate practical networking skills applicable to network support, help desk, network administration, and cybersecurity roles.

## Technologies & Skills Demonstrated

- Cisco Packet Tracer
- VLANs and network segmentation
- 802.1Q trunking
- Inter-VLAN routing
- Layer 3 switching
- Router-on-a-stick
- DHCP and DHCP relay
- Static routing
- WAN connectivity
- WPA2-PSK wireless security
- Voice VLANs
- Firewall security
- IP addressing and subnetting
- Network troubleshooting
- End-to-end connectivity testing
- Simulated Internet connectivity

---

## Network Topology

The network consists of an HQ environment and a Branch environment connected through a routed WAN. The design includes routers, Layer 2 and Layer 3 switches, servers, wireless access points, PCs, laptops, IP phones, and a firewall/Internet edge.

![Final Enterprise Network Topology](screenshots/1.Final%20enterprise%20network%20topology.png)

*Final enterprise network topology.*

---

## Headquarters Network

### VLAN Configuration

The HQ network uses separate VLANs to segment management, data, voice, server, and wireless traffic.

| VLAN | Name | Network |
|---|---|---|
| 10 | Management | 10.10.10.0/24 |
| 20 | HQ-DATA | 10.10.20.0/24 |
| 30 | HQ-VOICE | 10.10.30.0/24 |
| 40 | SERVER | 10.10.40.0/24 |
| 50 | WIRELESS | 10.10.50.0/24 |

![HQ VLAN Configuration](screenshots/2.HQ%20VLAN%20configuration.png)

*HQ VLAN configuration.*

### Inter-VLAN Routing

The HQ multilayer switch provides Layer 3 gateways for the VLANs and enables communication between authorized network segments.

![HQ Inter-VLAN Gateways](screenshots/3.HQ%20inter-VLAN%20gateways.png)

*HQ inter-VLAN gateways.*

### VLAN and Trunk Validation

802.1Q trunking carries multiple VLANs between the HQ access and core switches.

![HQ VLAN and Trunk Validation](screenshots/4.HQ%20VLAN%20and%20trunk%20validation.png)

*HQ VLAN and trunk validation.*

---

## DHCP Services

The HQ server provides centralized DHCP services for multiple network segments.

![HQ Centralized DHCP Pools](screenshots/5.HQ%20centralized%20DHCP%20pools.png)

*HQ centralized DHCP pools.*

DHCP relay allows clients located on different VLANs to reach the centralized DHCP server.

![HQ DHCP Relay](screenshots/6.HQ%20DHCP%20relay%20configuration.png)

*HQ DHCP relay configuration.*

---

## Wireless Security

The HQ wireless network uses WPA2-PSK with AES encryption.

![HQ WPA2 Wireless Security](screenshots/7.HQ%20WPA2%20wireless%20security.png)

*HQ WPA2 wireless security.*

> **Note:** The wireless credentials shown in this Packet Tracer lab are simulation-only credentials and are not used on a production network.

---

## HQ Connectivity Testing

Connectivity testing verifies successful communication between HQ network segments and services.

![HQ Inter-VLAN Connectivity](screenshots/8.HQ%20inter-VLAN%20connectivity.png)

*HQ inter-VLAN connectivity.*

### Voice VLAN

A dedicated voice VLAN separates IP phone traffic from regular data traffic.

![HQ Voice VLAN](screenshots/9.HQ%20voice%20VLAN%20validation.png)

*HQ voice VLAN validation.*

---

## Branch Network

### Router-on-a-Stick

The Branch uses router-on-a-stick with 802.1Q subinterfaces to route traffic between its VLANs.

| VLAN | Name | Network |
|---|---|---|
| 110 | BR-DATA | 10.20.10.0/24 |
| 120 | BR-VOICE | 10.20.20.0/24 |
| 130 | BR-WIFI | 10.20.30.0/24 |
| 199 | BR-MGMT | 10.20.99.0/24 |

![Branch Router-on-a-Stick](screenshots/10.Branch%20router-on-a-stick.png)

*Branch router-on-a-stick.*

### Branch VLAN and Trunk Validation

The Branch switch uses VLAN segmentation and an 802.1Q trunk toward the Branch router.

![Branch VLAN and Trunk](screenshots/11.Branch%20VLAN%20and%20trunk%20validation.png)

*Branch VLAN and trunk validation.*

### Branch Wireless Security

The Branch wireless network uses WPA2-PSK with AES encryption.

![Branch WPA2 Wireless Security](screenshots/12.Branch%20WPA2%20wireless%20security.png)

*Branch WPA2 wireless security.*

### Voice DHCP

The Branch router provides DHCP addressing for IP phones on the voice VLAN.

![Branch Voice DHCP](screenshots/13.Branch%20voice%20DHCP%20validation.png)

*Branch voice DHCP validation.*

---

## WAN and Routing

Static routing provides connectivity between the Headquarters and Branch networks across the WAN.

![HQ and Branch Routing](screenshots/14.HQ%20and%20Branch%20routing%20table.png)

*HQ and Branch routing table.*

### Branch-to-HQ Connectivity

End-to-end testing confirms that Branch devices can communicate with resources at Headquarters.

![Branch to HQ Connectivity](screenshots/15.Branch-to-HQ%20connectivity.png)

*Branch-to-HQ connectivity.*

---

## Internet Connectivity

The enterprise topology includes a simulated Internet edge and firewall. Connectivity tests verify external reachability from both sites.

### HQ Internet Connectivity

![HQ Internet Connectivity](screenshots/16.HQ%20Internet%20connectivity%20Verification.png)

*HQ Internet connectivity verification.*

### Branch Internet Connectivity

![Branch Internet Connectivity](screenshots/17.Branch%20Internet%20connectivity%20Verification.png)

*Branch Internet connectivity verification.*

---

## Validation Results

The completed lab successfully demonstrated:

- VLAN segmentation at HQ and Branch
- Inter-VLAN routing
- 802.1Q trunking
- Centralized DHCP and DHCP relay
- Router-on-a-stick
- Secure WPA2 wireless connectivity
- Voice VLAN addressing
- HQ-to-Branch WAN communication
- Static routing
- Firewall-protected network edge
- Simulated Internet connectivity from HQ and Branch

---

## Key Takeaways

This project strengthened my hands-on understanding of enterprise network design, configuration, segmentation, routing, wireless security, DHCP services, WAN connectivity, and systematic network troubleshooting.

It also provided practical experience validating configurations with Cisco IOS commands and end-to-end connectivity tests.

---

## Author

**Affissou Gbadamassi**

Cybersecurity & Networking Professional  
CompTIA Network+ | Cisco CCNA  
Master's in Cybersecurity
