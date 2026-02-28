# 🖧 ENCS304 – Computer Networks Lab
## 📌 Assignment 1: Basic Network Topologies Using Switches and Hubs

---

## 👨‍🎓 Student Details

| Field | Information |
|-------|-------------|
| Name | Priyanshu Tomar |
| Roll No. | 2301010162 |
| Program | B.Tech (CSE) |
| Semester | 6 |
| Course Code | ENCS304 |
| Course Name | Computer Networks Lab |
| School | School of Engineering and Technology |

---

## 🎯 Experiment Objective

The objective of this experiment was to design and analyze different LAN topologies to understand how network structure impacts connectivity, performance, packet flow behavior, and fault tolerance.

The networks were designed and tested using Cisco Packet Tracer.

---

## 🛠️ Equipment & Software Used

### Virtual Devices (Packet Tracer)
- PCs
- Cisco 2960 Switches
- Hub
- Copper Straight-Through Ethernet Cables

### Software
- Cisco Packet Tracer
- Windows Operating System

---

# 🌐 Topologies Implemented

## 1️⃣ Star Topology (Switch-Based)

Configuration:
- 1 Switch
- 4 PCs connected directly
- IP Range: 192.168.10.1 – 192.168.10.4
- Subnet Mask: 255.255.255.0 (/24)

Testing:
- Ping sent from PC1 → PC2, PC3, PC4
- All replies received successfully

Observations:
- No collisions
- Switch forwards frames using MAC Address Table
- If one cable disconnects → Only that PC is affected
- Better performance compared to hub

---

## 2️⃣ Bus-like Topology (Hub-Based)

Configuration:
- 1 Hub
- 4 PCs connected
- Same IP scheme used

Testing:
- Simultaneous ping between devices

Observations:
- Hub broadcasts packets to all ports
- Higher collision probability
- Lower performance
- If hub fails → Entire network fails

---

## 3️⃣ Ring-like Topology (Loop Using Switches)

Configuration:
- 3 Switches connected in loop
- 1–2 PCs attached per switch
- Subnet: 192.168.10.0/24

Testing:
- Ping across switches successful

Observations:
- Multiple communication paths available
- Improved fault tolerance
- Data reroutes if one link fails

---

# 🔍 Failure Test

One link in the ring topology was disconnected.

Result:
- Communication remained successful
- Traffic automatically used alternate path

This demonstrates better redundancy compared to hub-based and simple star topology.

---

# 📂 Repository Contents

- exp1_topologies.pkt → Packet Tracer network file
- output_exp1.txt → Ping outputs and observations
- report_exp1.pdf → Complete lab report with screenshots
- README.md → Project documentation

---

# ▶️ How to Open and Test

1. Install Cisco Packet Tracer
2. Open exp1_topologies.pkt
3. Click on any PC
4. Go to Desktop → Command Prompt
5. Run: ping <destination_IP>
6. Use Simulation Mode to observe packet flow

Example:
ping 192.168.10.2

---

# 📊 Learning Outcomes

✔ Designed multiple LAN topologies  
✔ Configured IPv4 addresses correctly  
✔ Verified connectivity using ICMP  
✔ Compared topology performance  
✔ Tested network fault tolerance  

---

# 📌 Conclusion

This experiment demonstrates how network topology affects performance, reliability, and scalability. Switch-based networks provide better efficiency, while loop designs offer improved redundancy.

EOF
