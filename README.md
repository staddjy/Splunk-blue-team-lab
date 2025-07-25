# 🛡️ Splunk Blue Team Lab

A hands-on cybersecurity lab simulating a blue team environment using Splunk for log collection, detection, and analysis.

---

## 📘 Project Overview

This lab is designed to simulate a real-world security operations environment. It leverages Splunk as a SIEM to monitor and analyze logs from a Windows machine using Sysmon and the Universal Forwarder.

---

## 🖥️ Lab Architecture

| Component        | IP Address     | Hostname     | Role         |
|------------------|----------------|--------------|--------------|
| SIEM (Splunk)     | 10.128.0.2     | staddjyc     | Log collection & analysis |
| Windows VM        | 10.128.0.3     | windows-vm   | Log generator (Sysmon)    |
| Attacker Machine  | 10.128.0.4     | kali/ubuntu  | Simulated attacker        |

---

## ⚙️ Tools & Technologies

- **Splunk Enterprise**
- **Splunk Universal Forwarder**
- **Windows Sysmon**
- **MITRE ATT&CK Framework**
- **PowerShell / CMD**
- **Ubuntu/Kali Linux**

---

## 📂 Data Collection

- Logs collected from Windows include:
  - Sysmon Event ID 1 (Process Creation)
  - Event ID 4624 (Logon)
  - Event ID 4798 (User Account Enumeration)
  - Registry changes, network connections, etc.

---

## 📊 Splunk Searches & Dashboards

Some example Splunk queries used in the project:

```spl
index=* host=windows-vm EventCode=4624
index=* host=windows-vm EventCode=4798
index=* sourcetype=WinEventLog:Security
