# Home Lab Setup with VirtualBox

## Overview
This project documents the setup of my personal home lab using VirtualBox, where I have configured:
- A **Windows 10 virtual machine** for security monitoring.
- A **Parrot OS virtual machine** for penetration testing.

## Virtual Machines

### 1. Windows 10 VM
- Installed **Splunk** for security monitoring.
- Installed **Sysmon** for advanced event logging and threat detection.
- Configured a **static IP address**.

### 2. Parrot OS VM
- Chose **Parrot OS** due to its built-in cybersecurity tools, similar to Kali Linux, but with additional penetration testing, forensics, and cryptography utilities.
- Configured a **static IP address**.

## Network Configuration
Both virtual machines are set to **Internal Network mode** to simulate a local network environment.

| Machine   | IP Address     | Netmask        |
|-----------|--------------|----------------|
| Windows 10 | 192.168.20.10 | 255.255.255.0 |
| Parrot OS  | 192.168.20.11 | 255.255.255.0 |

## Troubleshooting & Solution
- Initially, the **Linux VM could not ping the Windows VM** due to Windows Firewall blocking ICMP traffic.
- Instead of disabling the firewall, I tested network connectivity by **pinging the Linux VM from Windows**, which worked successfully.

## Future Plans
- Configure **Splunk** to collect and analyze logs from both machines.
- Enable **remote access** between the VMs for security testing.
- **Simulate cyber attacks** to generate security telemetry using:
  - **Nmap** for network scanning.
  - **MSFVenom** for payload creation.
- **Establish a reverse shell** on the Windows VM using the **Metasploit Framework**.
- Monitor security logs in **Splunk** and **Sysmon** to analyze how attacks are detected.
- Expand the lab with additional VMs for **SIEM monitoring and forensic analysis**.

---

This home lab serves as a foundation for security testing, monitoring, and hands-on cybersecurity learning.
