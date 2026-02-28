🖧 ENCS304 – Computer Networks
Assignment 1: Basic Network Topologies Using Switches and Hubs
👨‍🎓 Student Details

Name: Priyanshu Tomar
Roll no.:- 2301010162

Program: B.Tech (CSE)

Semester: 6

Course Code: ENCS304

Course Name: Computer Networks lAB

School: School of Engineering and Technology

🎯 Experiment Objective

This experiment was performed to understand how different LAN topologies affect:

Network connectivity

Performance

Packet flow behavior

Fault tolerance

The networks were designed and tested using Cisco Packet Tracer.

🛠️ Equipment & Software Used
💻 (Virtual Components in Packet Tracer)

PCs

Switches (Cisco 2960)

Hub

Ethernet Copper Straight-through Cables

🧰 Software Tool

Cisco Packet Tracer (Network Simulation Tool)

Windows Operating System

🌐 Topologies Implemented
1️⃣ Star Topology (Switch-Based)

Configuration:

1 Switch

4 PCs connected directly to switch

IP Address Range: 192.168.10.1 – 192.168.10.4

Subnet Mask: 255.255.255.0 (/24)

Testing:

Ping sent from PC1 to PC2, PC3, PC4

All replies received successfully

Observation:

No collisions

Switch forwards frames using MAC address table

If one cable disconnects → Only that PC is affected

2️⃣ Bus-like Topology (Hub-Based)

Configuration:

1 Hub

4 PCs connected to hub

Same IP scheme used

Testing:

Simultaneous ping between devices

Observation:

Hub broadcasts data to all ports

Higher collision possibility

Lower performance

If hub fails → Entire network fails

3️⃣ Ring-like Topology (Loop Using Switches)

Configuration:

3 Switches connected in loop

1–2 PCs attached per switch

Same subnet: 192.168.10.0/24

Testing:

Ping across different switches

Observation:

Multiple communication paths available

Better fault tolerance

Data can take alternate path

🔍 Failure Test

One link in the ring topology was disconnected.

Result:

Communication still successful

Traffic rerouted via alternate path

This shows better fault tolerance compared to hub and simple star topology.

exp1_topologies.pkt   → Packet Tracer network file  
output_exp1.txt       → Ping outputs and observations  
report_exp1.pdf       → Complete experiment report with screenshots  
README.md             → Project documentation  

▶️ How to Open and Test the Project

1️⃣ Install Cisco Packet Tracer
2️⃣ Download or clone this repository
3️⃣ Open file: exp1_topologies.pkt
4️⃣ Click on any PC
5️⃣ Go to:Desktop → Command Prompt
6️⃣ Type:ping <destination_IP>
7️⃣ To observe packet movement:

Switch to Simulation Mode

Use ICMP filter

Watch packet flow

📊 Learning Outcomes Achieved

✔ Designed multiple LAN topologies
✔ Configured IPv4 addresses correctly
✔ Verified connectivity using ICMP
✔ Understood packet flow differences
✔ Compared topology performance
✔ Tested network fault tolerance

📌 Practical Applications

Office LAN design

Computer Lab networking

Understanding cost vs performance trade-offs

Basic physical network planning

📎 Conclusion

This experiment successfully demonstrated how topology selection impacts:

Performance

Reliability

Cost

Fault tolerance

Switch-based star topology offers better performance than hub-based networks, while ring-like topology provides better redundancy.


