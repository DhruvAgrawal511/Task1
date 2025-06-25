# Task 1 – Local Network Port Scan

## Objective
Discover open ports on devices in the local network using Nmap to understand network exposure and potential risks.

---

## Tools Used
- [Nmap](https://nmap.org/) – For scanning devices and open ports.
- Kali Linux (pre-installed Nmap)

---

## Steps Followed

1. **Checked Network Interface and IP Range**
   ```bash
   ip a
  - identified subnet: 192.168.31.196/24

2. **Performed TCP SYN Scan**
   ```bash
   sudo nmap -sS 192.168.1.0/24
3. **Saved Output (As .txt file)**
   ```bash
   sudo nmap -sS 192.168.1.0/24 -oN scan_result.txt


## Security Risks
### Open Ports:

- 53/tcp (DNS) – Can be used in DNS amplification attacks if misconfigured.
- 80/tcp (HTTP) – Unencrypted, vulnerable to man-in-the-middle (MITM) attacks.
- 443/tcp (HTTPS) – Secure if configured properly with valid certificates.
- 7443/tcp (oracleas-https) – Often used by admin panels (e.g., Ubiquiti, Oracle apps). Can be high risk if exposed.
- 8080/tcp (HTTP-Proxy) – Often runs admin UIs (e.g., Tomcat). Check for weak auth.
- 8443/tcp (HTTPS-Alt) – Alternate secure web service. Confirm it doesn't expose sensitive interfaces.

## Key Concepts
  - Port Scanning
  - TCP SYN Scan
  - IP Ranges and Subnetting
  - Network Reconnaissance
  - Open Port Security Risks



