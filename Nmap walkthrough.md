# Nmap Cheat Sheet - PortSwigger Authentication Vulnerability Labs

## Introduction
This repository provides a detailed reference guide for **Nmap**, a powerful network scanning tool, specifically focused on **authentication vulnerability labs** from PortSwigger. The document covers essential Nmap switches, scan types, and relevant networking concepts.

---
## Networking Basics
### Q1: What networking constructs are used to direct traffic to the right application on a server?
**A:** Ports

### Q2: How many ports are available on any network-enabled computer?
**A:** 65,535

### Q3: How many of these are considered "well-known"?
**A:** 1,024

---
## Nmap Switches
### Q4: What is the first switch listed in the help menu for a 'SYN Scan'?
**A:** `-sS` (Finds out if a port is open, closed, or blocked without making a full connection.)

### Q5: Which switch would you use for a UDP scan?
**A:** `-sU` (Used to find open UDP ports on a server.)

### Q6: If you wanted to detect which operating system the target is running on, which switch would you use?
**A:** `-O` (Identifies the operating system, e.g., Windows, Linux, macOS.)

### Q7: Which switch detects the version of services running on the target?
**A:** `-sV`

### Q8: How do you increase verbosity in Nmap?
**A:** `-v`

### Q9: How do you set verbosity to level 2?
**A:** `-vv`

### Q10: What switch saves Nmap results in three major formats?
**A:** `-oA`

### Q11: What switch saves results in "normal" format?
**A:** `-oN`

### Q12: What switch saves results in "grepable" format?
**A:** `-oG`

### Q13: How do you enable "aggressive" mode?
**A:** `-A` (Enables OS detection, version detection, script scanning, and traceroute.)

### Q14: How do you set the timing template to level 5?
**A:** `-T5` (Fastest scan, but noisy.)

### Q15: How do you scan only port 80?
**A:** `-p80`

### Q16: How do you scan ports 1000-1500?
**A:** `-p1000-1500`

### Q17: How do you scan all ports?
**A:** `-p-`

### Q18: How do you activate a script from the Nmap scripting library?
**A:** `--script`

### Q19: How do you activate all scripts in the "vuln" category?
**A:** `--script=vuln`

### Q20: Which RFC defines the appropriate behavior for the TCP protocol?
**A:** RFC 9293

### Q21: If a port is closed, which flag should the server send back?
**A:** `RST` (Reset flag)

---
## SYN Scans
### Q22: What are two other names for a SYN scan?
**A:** Half-open scan, Stealth scan

### Q23: Can Nmap use a SYN scan without sudo permissions?
**A:** No

---
## UDP Scans
### Q24: If a UDP port doesn’t respond to an Nmap scan, what will it be marked as?
**A:** `open|filtered`

### Q25: When a UDP port is closed, which protocol sends a "port unreachable" message?
**A:** ICMP (Internet Control Message Protocol)

---
## NULL, FIN, and Xmas Scans
### Q26: Which of the three scan types uses the URG flag?
**A:** Xmas scan

### Q27: Why are NULL, FIN, and Xmas scans generally used?
**A:** Firewall evasion

### Q28: Which common OS responds with RST to NULL, FIN, or Xmas scans?
**A:** Microsoft Windows

---
## ICMP Network Scanning
### Q29: How would you perform a ping sweep on the `172.16.x.x` network?
**A:** `nmap -sn 172.16.0.0/16`

### Q30: What language are NSE scripts written in?
**A:** Lua

### Q31: Which category of scripts should not be run in a production environment?
**A:** Intrusive

### Q32: What optional argument can the `ftp-anon.nse` script take?
**A:** `maxlist`

### Q33: What is the filename of the script that determines the OS of an SMB server?
**A:** `smb-os-discovery.nse`

### Q34: What does `smb-os-discovery.nse` depend on?
**A:** `smb-brute`

---
## Advanced Nmap Features
### Q35: Which simple and frequently used protocol is often blocked, requiring the use of `-Pn`?
**A:** ICMP (Ping protocol)

### Q36: Which Nmap switch appends an arbitrary length of random data to packets?
**A:** `--data-length`

### Q37: Does the target IP respond to ICMP echo (ping) requests?
**A:** No

### Q38: How many ports are shown as open or filtered in an Xmas scan on the first 999 ports?
**A:** 999

### Q39: Why are all ports shown as open|filtered?
**A:** No response from the target

### Q40: How many open ports are detected in a TCP SYN scan on the first 5000 ports?
**A:** 5

### Q41: Can Nmap successfully log in to the FTP server on port 21 using the `ftp-anon` script?
**A:** Yes

---
## Conclusion
This guide serves as a **comprehensive reference** for using **Nmap** in **PortSwigger authentication vulnerability labs**. It covers networking fundamentals, various scanning techniques, and Nmap scripting capabilities.

🚀 **Happy Hacking & Stay Ethical!** 🔥

