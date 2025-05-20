# Nmap-Network-Scan-on-Kail-


# Project Overview
This project provides an introduction to Nmap, a powerful and widely used network scanning tool, along with practical examples of how to use it for network discovery, service/version detection. The included commands demonstrate common Nmap usage scenarios that are essential for network administrators. 


# What is Nmap?
Nmap (Network Mapper) is an open-source utility for network discovery and security auditing. It is used to:
-Discover hosts and services on a computer network
-Perform port scanning to find open ports
-Detect service versions and operating systems
-Identify vulnerabilities and misconfigurations

---

##  Tools Used

- **Nmap** – Network exploration tool and security/port scanner.
- **Linux terminal** – Bash shell for command-line input.


##  Installation

```bash
sudo apt-get update && sudo apt-get install nmap
````

Verify installation:

```bash
nmap -h
```

---

##  Commands

###  1. Scan an entire subnet

```bash
nmap 192.168.211.0/24
```

###  2. Service/version detection on a specific host

```bash
nmap -sV 192.168.211.254
```

###  3. ICMP ping scan (host discovery only, no port scan)

```bash
sudo nmap -PE -sn 192.168.211.254
```

###  4. Scan without DNS or ping (stealthy)

```bash
nmap -Pn -n 192.168.211.254
```

###  5. Aggressive scan on entire subnet (OS, version, scripts)

```bash
sudo nmap -A 192.168.1.0/24
```

###  6. TCP connect scan on specific ports in a subnet

```bash
sudo nmap -sT -p 192,18,68 192.168.1.0/24
```

###  7. Stealthy SYN scan on common ports

```bash
sudo nmap -sS -p 22,80,443 192.168.1.1
```

###  8. SYN scan with debug output
