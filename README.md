# 🔐 Wazuh SIEM Cybersecurity Lab

This project simulates a real-world security monitoring environment using **Wazuh**, an open-source Security Information and Event Management (SIEM) and Extended Detection and Response (XDR) platform. The lab explores event detection, threat hunting, and alert analysis across both **Linux (Ubuntu)** and **Windows Server** environments.

## 📚 Overview

The lab demonstrates how to:

- Configure Wazuh server and Windows agent communication
- Ingest and analyze security event logs
- Use advanced search queries in the Wazuh Discovery dashboard
- Detect key security events such as:
  - `ERROR` severity logs
  - Login failures and successes
  - Brute-force attacks
- Understand and use fields like:
  - `data.win.system.eventID`
  - `data.win.system.severityValue`
  - `rule.level`
- Filter, format, and visualize event data for investigation

## 🛠️ Tools & Technologies

- **Wazuh SIEM/XDR**
- **Windows PowerShell**
- **Ubuntu Terminal**
- **Wazuh Discovery Dashboard**
- **Remmina RDP Client**

## 🧪 Key Scenarios

- 🔍 Search for high-severity alerts using `rule.level`
- 🔐 Identify successful logins with `eventID:4624`
- 🚫 Investigate login failures and brute-force attempts (`eventID:4625`)
- 🧹 Filter noisy alerts using Boolean logic and wildcards
- 📅 Refine queries with date ranges and timestamps (`@timestamp`)
- 📊 Format results into custom tables for clarity

## 💡 Challenge Exercise

A brute-force attack scenario targeting three user accounts (`Cybrary`, `Guest`, and `Administrator`) was identified using:
Wazuh Query Language:
@timestamp > "2023-11" AND rule.mitre.technique:Brute Force
