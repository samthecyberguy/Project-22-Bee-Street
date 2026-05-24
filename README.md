# Project 22 Bee Street

## Overview

This project simulates a real-world cloud security monitoring environment using AWS, Cowrie, and SIEM technologies. The lab captures and analyzes real SSH attack traffic targeting internet-facing cloud infrastructure.

---

## Objectives

- Deploy a cloud-hosted SSH honeypot
- Capture real attack traffic
- Analyze brute-force behavior
- Build SOC-style detections
- Visualize attacker telemetry
- Develop hands-on cloud security skills

---

## Architecture

```text
Internet
    ↓
AWS EC2 Instance
    ↓
Cowrie Honeypot (Port 22)
    ↓
JSON + Log Telemetry
    ↓
SIEM / Dashboards / Detection Rules
```

---

## Technologies Used

| Technology | Purpose |
|---|---|
| AWS EC2 | Cloud infrastructure |
| Ubuntu Linux | Server operating system |
| Cowrie | SSH/Telnet honeypot |
| OpenSSH | Secure administration |
| Python | Automation and parsing |
| Wazuh / ELK | SIEM and monitoring |

---

# Phase 1 — Honeypot Deployment & SSH Hardening

## Goals
- Deploy AWS EC2 instance
- Configure security groups
- Harden SSH access
- Deploy Cowrie
- Separate real SSH from honeypot traffic

## Implemented
- Moved real SSH to port 2222
- Disabled root login
- Restricted admin access by source IP
- Deployed Cowrie on port 22
- Verified live attack traffic

## Key Skills
- Linux administration
- Cloud networking
- SSH hardening
- Security architecture

---

# Phase 2 — Log Collection & Threat Analysis

## Goals
- Parse Cowrie logs
- Analyze attacker IPs
- Track login attempts
- Extract attack patterns

## Planned Features
- GeoIP enrichment
- Username/password analysis
- Threat statistics
- Attack frequency tracking

---

# Phase 3 — SIEM Integration

## Goals
- Centralize logs
- Build detections
- Create dashboards
- Simulate SOC monitoring

## Planned Technologies
- Wazuh
- ELK Stack
- Splunk
- Microsoft Sentinel

---

# Phase 4 — Threat Visualization

## Goals
- Build attack dashboards
- Visualize attacker geography
- Display brute-force trends
- Analyze attacker behavior

---

# Phase 5 — Advanced Cloud Security Engineering

## Goals
- Infrastructure as Code
- Automated detections
- IDS/IPS integration
- Multi-honeypot deployment
- CloudWatch integration

---

# Example Attack Logs

```text
New connection: 185.x.x.x
Remote SSH version: SSH-2.0-libssh2
Connection lost after 0.2 seconds
```

---

# Learning Outcomes

This project demonstrates hands-on experience with:

- AWS cloud infrastructure
- Linux administration
- SSH hardening
- Honeypot deployment
- SIEM workflows
- Threat monitoring
- Detection engineering
- Security operations

---

# Future Improvements

- Malware analysis
- Threat intelligence feeds
- Automated blocking
- Kubernetes honeypots
- Multi-region deployment

---

# Author

Samuel Webster
