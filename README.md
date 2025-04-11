# Network_Scanning_nmap
Scanned local network using Nmap and documented findings with security insights.
# Network Scanning Project (Nmap)

# Objective
Use `nmap` to scan a local home network, discover live hosts, open ports, and running services. Document findings and reflect on security implications.

# Tools Used
- Kali Linux (2024)
- Nmap 7.95

# Scan Command

nmap -sV -T4 -Pn 192.168.178.0/24

# Results

IP Address      Ports Open      Services Detected       Notes
192.168.178.1   3306    MySQL (unauthorized)    Database Server
192.168.178.2   53      tcpwrapped      Possibly DNS
192.168.178.254 None    None    Filtered ports
192.168.178.136 None    None    Target Machine

# Analysis
192.168.178.1: MySQL (port 3306) is open. If exposed without proper authentication, it could be a target. Recommend restricting access and securing the database.

192.168.178.2: Port 53 (possibly DNS) is tcpwrapped. Indicates basic protection is in place but should be verified.

192.168.178.254 & 192.168.178.136: No open ports. Likely filtered or secured hosts. No immediate threats found. 
