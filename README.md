# Footprinting-and-Reconnaissance-Lab
Week 2 Cybersecurity Project – Footprinting and Reconnaissance using Kali Linux tools.

# PENETRATION TESTING REPORT 
**Footprinting & Network Scanning Phases**  
**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

| Field | Detail |
| :--- | :--- |
| **Pentester Name (Cybersecurity Professional)** | [madina] |
| **Program/Batch** | B084-Networkwalks |
| **Date** | 11 November 2026 |
| **Modules completed** | W2-PM1 (Multiple Kali Tools) |
| **Client/Target** | 1. Networkwalks (authorized assessment, subject to written permission) <br> 2. My own local LAN Network |
| **Permission secured from client?** | Confirmed only where written permission has been obtained |
| **Phases covered** | Phase 1: Reconnaissance & Footprinting <br> Phase 2: Scanning & Network Discovery <br> Phase 3-5: In Progress |

---

## 1. Liability Disclaimer

I have performed these activities only on systems and devices where I had secured written permission or on devices and systems that I own. All materials are strictly for educational and research purposes. The instructor, authors, and NetworkWalks bear no responsibility for how this knowledge is applied. Every action taken is the sole responsibility of the operator. Unauthorized system access is illegal and punishable by law.

## 2. Introduction

This report details the footprinting of the `networkwalks.com` domain using Kali Linux tools (W2-PM1) and the scanning of a local network using Zenmap (W2-PM5). The objective is to demonstrate the methodology an attacker uses to progress from passive information gathering to mapping live hosts on an active network. This work represents the Week 2 requirements of the ongoing internship program at NetworkWalks.

All commands were executed within Kali Linux and Windows environments. Each section documents the exact command issued, observed output, screenshot evidence, and a brief analysis of the security implications.

---

## 3. Tools Used

The table below outlines each tool utilized during the assessment alongside its specific operational function.

| Tool | Purpose |
| :--- | :--- |
| **Kali Linux & Windows** | Primary operating systems for reconnaissance activities |
| **WHOIS** | Domain registration lookup (owner information, creation dates, name servers) |
| **WhatWeb** | Web technology fingerprinting (web server, CMS, plugins, IP) |
| **nslookup** | DNS resolution of target domain names to IP addresses |
| **curl -I** | HTTP response header inspection |
| **wafw00f** | Web Application Firewall (WAF) detection |
| **dnsrecon** | DNS record enumeration (NS, MX, SPF, TXT) |
| **Zenmap (Nmap GUI)** | Subnet scanning to discover live hosts, IP, and MAC addresses |
| **Windows CMD** | Local network IP and MAC address verification |

---

## 4. Activities Performed

### 4.1 Footprinting & Reconnaissance

Reconnaissance was conducted against `networkwalks.com` using six Kali Linux security tools: WHOIS, WhatWeb, Nslookup, Curl, WafW00F, and DNSRecon. Each tool was deployed to extract distinct target details.

* **WHOIS:** Retrieved publicly available registration data and authoritative name servers.
* **WhatWeb:** Identified underlying web technologies, including WordPress and associated plugins.
* **Nslookup:** Resolved the domain name to its corresponding IP address.
* **Curl (-I):** Evaluated HTTP response headers and identified publicly exposed HTTP information.
* **WafW00F:** Checked for the presence of an active Web Application Firewall.
* **DNSRecon:** Enumerated DNS records, retrieving mail servers, SPF/TXT records, and DNS configuration data.

### 4.2 Network Scanning with Zenmap

Network discovery was performed on the local subnet to identify active hosts, IP addresses, MAC addresses, and overall network topology.

1. Executed `ipconfig` in the Windows terminal to determine the local IP address and subnet mask.
2. Configured Zenmap with the local subnet target and initiated a **Ping Scan** to locate live systems.
3. Identified active devices on the local network and examined their corresponding IP addresses and MAC addresses.
4. Generated and saved the graphical network structure using the **Topology** viewer in Zenmap.

---

## 5. Recommendations

Based on the security assessment, the following remediation measures are recommended:

1. **Restrict Public Metadata:** Minimize unnecessary public exposure of web framework versions, CMS details, and internal application paths.
2. **Maintain Patch Management:** Keep all CMS platforms, plugins, and dependencies updated to protect against known vulnerabilities.
3. **Harden HTTP Headers:** Configure appropriate HTTP response headers to reduce information leakage regarding underlying server infrastructure.
4. **Audit DNS Records:** Periodically review DNS records to ensure only necessary services are publicly resolvable.
5. **Optimize WAF Rulesets:** Maintain active WAF rulesets to detect and filter malicious traffic effectively.

---

## 6. Conclusion

The activities completed during Week 2 provided practical experience in footprinting, passive reconnaissance, and active network scanning.

Reconnaissance is a vital phase of ethical hacking. Analyzing publicly accessible resources and network responses yields useful insights into a target environment before any further security assessment.

Clear documentation of technical findings ensures that security risks are properly understood and effectively mitigated within an authorized scope.

---

## 7. Evidences Collected

Screenshots collected as evidence during the activities (stored in the `screenshots/` folder):
![Screenshot 1](Screenshot%201.png)
![Screenshot 2](Screenshot%202.png)
![Screenshot 3](Screenshot%203.png)
![Screenshot 4](Screenshot%204.png)
![Screenshot DNS](Screenshot%20dns.png)
![Screenshot 2026-11-12 060526](Screenshot%202026-11-12%20060526.png)
![Screenshot 2026-11-12 064256](Screenshot%202026-11-12%20064256.png)
Learning by doing. Investigating by understanding
