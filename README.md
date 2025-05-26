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
