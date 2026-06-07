# Networking Internship Task 1 Report
**Date:** June 5, 2026  
**Intern:** Hansini Kulal  
---
## 🎯 Task Objectives
* Understand the fundamental concepts and components of computer networks.
* Identify and examine the local network configuration of a system.
* Learn and define essential networking terms, devices, and protocols.
* Create a visual representation of the network connection architecture.
* Perform basic network troubleshooting using diagnostic commands and analyze the results.
* Organize project documentation systematically and publish it to a GitHub repository.
---
## 🛠️ Tools and Commands Used
* **`ipconfig` / `ifconfig`** – Network interface configuration tool
* **`ping`** – ICMP network connectivity tester
* **`traceroute` / `tracert`** – Packet route path diagnostic utility
* **Canva / Draw.io** – Network diagram architecture designer
---
## 💻 Network Setup
Below are the network configuration details extracted from the local host system's primary active interface (**Wireless LAN adapter Wi-Fi**):

| Property | Configuration Value |
| :--- | :--- |
| **Hostname (Device Name)** | Windows PC |
| **IPv4 Address** | 10.144.211.176 |
| **MAC Address** | 00:1A:2B:3C:4D:5E |
| **Default Gateway** | 10.144.211.120 |
| **DNS Server** | *Not Listed* |

> **Note:** The host system also displays virtual network configurations for VMware environments (`VMnet1` and `VMnet8`).
<img width="1100" height="615" alt="Screenshot 2026-06-07 220150" src="https://github.com/user-attachments/assets/9dfaee2d-3d8c-4fa7-937c-e94421738556" />

---
## 🌐 Basic Networking Concepts
* **IP Address:** A unique numerical identifier assigned to a device on a network, enabling communication between devices.
* **MAC Address:** A unique hardware address assigned to a network interface by the manufacturer for device identification.
* **Default Gateway:** A network device, typically a router, that directs traffic from a local network to external networks.
* **DNS (Domain Name System):** A service that converts domain names (e.g., google.com) into IP addresses.
* **Private IP Address:** An IP address used within a local network that is not directly accessible from the internet.
* **Public IP Address:** A globally unique IP address assigned by an ISP, used to identify a network on the internet.
---
## ⚡ Network Connectivity & Diagnostics Test
### 1. Packet Loss Test (ping)
* **Command Executed:** `ping google.com`
* **Result Analysis:** The ping was successful with 0% packet loss. Packets Sent = 4, Received = 4, Lost = 0.
* **Latency:** Minimum = 63ms, Maximum = 196ms, Average = 126ms. This confirms that the internet connection is active and responsive.
  <img width="858" height="377" alt="Screenshot 2026-06-07 220500" src="https://github.com/user-attachments/assets/7e739307-6a6f-4752-8192-383cf48b1869" />

### 2. Path Route Diagnostics (tracert)
* **Command Error Troubleshooting:** Running traceroute google.com directly in Windows Command Prompt returned an error because traceroute is a native Linux/macOS command.
* **Resolution:** Switched to the native Windows equivalent utility tracert google.com which executed successfully.
* **Route Path Log:** The packet reached the final Google destination server (bom05s12-in-x0e.1e100.net) in exactly 17 hops.
  <img width="1049" height="522" alt="Screenshot 2026-06-07 220720" src="https://github.com/user-attachments/assets/65fcf9e8-dc90-4426-af17-7b0acee0c201" />

---
## ❓ Question and Answers
### Q1: Was the ping successful?
**A:** Yes, the ping was successful with 0% packet loss, which means the connection is working.  
### Q2: How many hops were shown?
**A:** There were 17 hops shown in the tracert diagnostic log, which means the data packet passed through 17 intermediate steps/routers to reach the destination server.
### Q3: What is the purpose of traceroute?
**A:** Traceroute is used to track how data travels from one device to another. It records and displays the path taken by packets across an IP network, helping pinpoint network bottlenecks or routing drops.
