# SIEM Deployment & SSH Brute Force Detection with Splunk

> A hands-on SOC project focused on centralized log monitoring, SSH security analysis, brute-force detection, alerting, and dashboard visualization using Splunk Enterprise.

---

## 📌 Project Overview

This project consists of building a small Security Operations Center (SOC) laboratory using **Splunk Enterprise** as a Security Information and Event Management (SIEM) platform.

The objective is to collect Linux authentication logs, forward them to a centralized SIEM, analyze SSH authentication activity, detect repeated failed login attempts, generate a security alert, and visualize the activity through a SOC dashboard.

The project demonstrates an end-to-end security monitoring workflow:

**Log Collection → SIEM → Analysis → Detection → Alerting → Visualization**

---

## 🎯 Objectives

- Deploy and configure Splunk Enterprise as a SIEM platform.
- Configure a Splunk Universal Forwarder.
- Collect Linux authentication logs.
- Forward authentication events to the SIEM.
- Analyze SSH authentication activity using SPL.
- Detect repeated failed SSH login attempts.
- Configure an automated security alert.
- Build a SOC monitoring dashboard.
- Perform a controlled security test.

---

## 🏗️ Lab Architecture

The laboratory contains two main virtual machines:

| Component | Role |
|---|---|
| Kali Linux | Log source and controlled SSH testing |
| Ubuntu Server | Centralized Splunk SIEM server |
| Splunk Universal Forwarder | Log collection and forwarding |
| Splunk Enterprise | SIEM, detection, alerting and visualization |

### Architecture Flow

```text
Kali Linux
    │
    │ Authentication Logs
    ▼
/var/log/auth.log
    │
    ▼
Splunk Universal Forwarder
    │
    │ TCP 9997
    ▼
Ubuntu Server
    │
    ▼
Splunk Enterprise
    │
    ├── Log Analysis
    ├── Brute Force Detection
    ├── Security Alert
    └── SOC Dashboard
