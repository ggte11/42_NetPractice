*This project has been created as part of the 42 curriculum by mcardoso.*

# NetPractice

## Description

NetPractice is a system administration and networking project from the 42 curriculum. The goal is to solve a series of networking puzzles by correctly configuring small virtual networks so that all hosts can communicate with each other.

Each level presents a broken network topology — with misconfigured IP addresses, subnet masks, or routing tables — and the task is to identify and fix the issues so that every device can reach every other device in the network. The project covers 10 progressive levels, each introducing new complexity in terms of routing, subnetting, and network topology.

By completing this project, you gain hands-on understanding of how IP networks are structured and how packets are routed from source to destination.

## Instructions

### Running the Training Interface

A shell script is provided to launch the training interface locally in your browser:

```bash
bash run.sh
```

This will open the NetPractice interface at `http://localhost:8080` (or similar). From there, select a level to begin configuring the network.

### Solving and Exporting Configurations

1. Open a level in the training interface.
2. Fill in the missing or incorrect values (IP addresses, subnet masks, routes) until the network is valid.
3. Once the level is solved, click the **"Get my config"** button to export your configuration.
4. Save the exported file — it will be named after the level (e.g., `level1.json`).
5. Repeat for all 10 levels.

### Submission Requirements

- Solve all 10 levels and export a configuration file for each one
- Place all 10 exported configuration files at the **root of your Git repository**
- Files should be named as provided by the export function (e.g. `level1.json` through `level10.json`)
- Include this `README.md` at the root of the repository as well

## Resources

### Networking Concepts Studied

This project covers the following networking fundamentals:

- **TCP/IP Addressing** — Understanding IPv4 address structure (32-bit, dotted-decimal notation), address classes, and how addresses identify hosts on a network.
- **Subnet Masks & CIDR** — Using subnet masks (e.g., `255.255.255.0`) and CIDR notation (e.g., `/24`) to divide networks into subnets and determine the range of valid host addresses.
- **Network & Broadcast Addresses** — Identifying the network address (first) and broadcast address (last) within a subnet, and understanding which addresses are assignable to hosts.
- **Default Gateways** — How hosts forward traffic destined for outside their local subnet to a gateway (router interface).
- **Routers & Switches** — The role of routers in forwarding packets between different networks using routing tables, versus switches operating at Layer 2 within a single network.
- **Point-to-Point Links** — Configuring /30 subnets for direct links between two routers.
- **Routing Tables** — How routers and hosts use destination/mask/next-hop entries to decide where to send packets, including the use of the default route (`0.0.0.0/0`).
- **Public vs. private IP addresses** — RFC 1918 reserved ranges (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16) and why they are not routable on the public internet
- **OSI Model Layers** — Conceptual understanding of the 7-layer model, with focus on Layer 2 (Data Link / MAC addressing) and Layer 3 (Network / IP routing).

- **NAT (Network Address Translation)** — conceptual understanding of how private networks reach the internet by rewriting source addresses at the border router

### Reference Documentation & Tutorials

- **TCP/IP Model — GeeksforGeeks**
  https://www.geeksforgeeks.org/computer-networks/tcp-ip-model/
  Overview of the TCP/IP stack, its layers, and how addressing operates at the network layer.

- **TCP/IP Addressing — IBM AIX Documentation**
  https://www.ibm.com/docs/en/aix/7.2.0?topic=protocol-tcpip-addressing
  Technical reference on IPv4 address classes, subnet masks, and how addressing is applied in practice.

- **Networking Fundamentals — YouTube Playlist (Practical Networking)**
  https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P
  Video series covering subnetting, routing, switching, and TCP/IP fundamentals with visual explanations.

### AI Usage

AI was used in this project for the following:

- **Concept clarification** — Asking targeted questions to deepen understanding of subnetting, CIDR notation, and routing table logic when certain levels were unclear.
- **Verification** — Double-checking subnet calculations and route configurations to validate reasoning before submitting answers in the interface.
