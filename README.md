# Inter-VLAN Routing using 802.1Q (Router-on-a-Stick)

This repository features a **Cisco Packet Tracer** network topology demonstrating **Inter-VLAN routing** using a single physical router interface split into logical subinterfaces (**Router-on-a-Stick** configuration).

## 📁 Repository Structure
*   `vlan_routing_topology.pkt` - The complete Cisco Packet Tracer lab file.
*   `topology.png` - Visual map layout of the network infrastructure.
*   `ping-verification.png` - Screenshot proof of successful end-to-end communication tests.

## 🌐 Topology Overview
The network is segmented into three distinct Virtual Local Area Networks (VLANs) utilizing `/26` subnets:
*   **VLAN 10:** `10.0.0.0/26` (Hosts: PC1, PC0, PC5, PC6)
*   **VLAN 20:** `10.0.0.64/26` (Hosts: PC4)
*   **VLAN 30:** `10.0.0.128/26` (Hosts: PC3, PC2)

## 🛠️ Key Technologies & Concepts Used
*   **Router-on-a-Stick (ROAS):** Configured logical subinterfaces on the router's physical interface (`g0/1`) to route traffic between different broadcast domains.
*   **IEEE 802.1Q (dot1q):** Applied industry-standard encapsulation protocols on subinterfaces to tag inter-VLAN traffic correctly.
*   **Trunking Ports:** Configured high-bandwidth connections between switches (`Switch1` and `Switch2` via `g0/1` and `g0/2`) and the link leading to the router to carry traffic for multiple VLANs simultaneously.

## 🚀 Verification & Results
All configurations were verified using ICMP ping tests from the command line, confirming successful inter-VLAN routing communication:
*   **VLAN 10 Gateway (10.0.0.1):** 0% loss;

