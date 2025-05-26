# Elevate-labs
Cybersecurity Internship
Task 1

Objective
Perform a TCP SYN scan on the local network using Nmap to identify active devices, discover open ports, and assess potential security risks.

---

Tools Used
- Nmap
- Command Line (Windows)
- Optional: Wireshark (not used in this task)

---

Network Details

- **Scanned Range:** `192.168.1.0/24`
- **Device IP:** `192.168.1.2`

---

 Nmap Command Used

```bash
nmap -sS 192.168.1.0/24 -oN scan_result.txt


Scan Summary
| IP Address  | Open Ports                       | Device Info                  |
| ----------- | -------------------------------- | ---------------------------- |
| 192.168.1.1 | 53 (DNS), 80 (HTTP), 443 (HTTPS) | Router (GX International BV) |
| 192.168.1.2 | 135, 139, 445, 902, 912, 3306    | My Windows PC                |
| 192.168.1.3 | None (All ports closed)          | Unknown                      |
| 192.168.1.7 | 139 (Filtered)                   | Unknown                      |


Security Risks Identified
Router (192.168.1.1):

HTTP (80) is unencrypted, which could expose login interfaces if remote access is enabled.

DNS (53) open — if misconfigured, could be abused in DNS amplification attacks.

My PC (192.168.1.2):

Ports 135, 139, 445 (MSRPC, NetBIOS, SMB) are commonly targeted by malware and lateral movement.

Port 3306 (MySQL) exposed — may allow unauthorized access to databases if not properly secured.

902/912 are related to virtualization or remote access — verify their necessity.


 Files Included
scan_result.txt — Raw Nmap scan output.

README.md — Explanation and analysis.

