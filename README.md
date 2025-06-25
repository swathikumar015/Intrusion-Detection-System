# 🛡️ Intrusion Detection System (IDS)

> ⚡ Real-time detection of **Port Scans**, **SYN Floods**, and **DNS Spoofing** using Python & Scapy  
> 👩‍💻 Lightweight. Dependency-Free. Packet-Level Awareness.

---

## 🧠 Overview

Modern networks are constantly targeted by stealthy low-level attacks that evade traditional firewalls and antivirus software. This project presents a **lightweight, real-time Intrusion Detection System (IDS)** designed to detect:

- 🚨 **Port Scans** 
- 🌊 **SYN Floods** 
- 🎭 **DNS Spoofing** 

Developed in **Python** using the **Scapy** packet manipulation library, this IDS monitors live traffic and flags suspicious activity using rule-based heuristics — **no bulky signatures or external databases** required.

---

## 🎯 Problem Statement

Traditional security mechanisms often **fail to detect low-level network anomalies** that precede more serious breaches. This includes:

- **Excessive SYN packets** from a single source (port scans)
- **Rapid, repeated TCP handshakes** without completions (SYN floods)
- **Mismatch between DNS queries and response IPs** (DNS spoofing)

These attacks can disrupt availability, compromise sensitive data, or serve as backdoors for attackers.

---

## ✅ Solution Highlights

| Feature        | Description |
|----------------|-------------|
| 🔍 Live Packet Sniffing | Captures traffic on selected network interfaces using Scapy |
| 🧠 Intelligent Heuristics | Detects patterns in packet metadata to infer malicious behavior |
| ⚠️ Real-Time Alerts | Real-time monitoring using Wireshark |
| 🪶 Lightweight & Transparent | No external signatures or heavy dependencies |

---

## 🛠️ Technologies Used

- **Python 3.x**
- **[Scapy](https://scapy.readthedocs.io/)** – Packet sniffing, dissection, and analysis
- Runs on **Linux, Mac, and Windows** with `sudo`/admin privileges

---

## 🚀 How It Works

## 🔐 Detection Modules

1. **Port Scan Detection**
   - 🔎 Attackers send requests to many ports on a device to find open and vulnerable ones.
   - 📍 This module checks for unusually high numbers of connection attempts (SYN packets) to multiple ports from a single source IP.

2. **SYN Flood Detection**
   - 🌊 A form of DoS (Denial-of-Service) attack where the attacker sends too many TCP connection requests (SYN packets) but never completes them.
   - 💥 This overloads the system’s resources, making it slow or unresponsive.

3. **DNS Spoofing Detection**
   - 🎭 In this attack, fake DNS responses are sent to trick a device into thinking a website (like `example.com`) points to a malicious IP address.
   - 🛡️ The system checks whether the returned IP for a domain matches a trusted IP, and raises an alert if it doesn’t.


