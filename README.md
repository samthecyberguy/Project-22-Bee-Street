# Cloud-Honeypot-SOC-Lab-1
An AWS EC2 instance hosting the Cowrie honeypot listening on port 22, posing as a legitimate SSH server.  Utilizing Wazuh and Kibana for attack analysis. 
Project Overview

This project simulates a real-world cloud security monitoring environment using an AWS-hosted SSH honeypot, centralized logging, attack analysis, and SOC-style detections. The lab is designed to study internet-wide automated attacks against cloud infrastructure while developing practical cloud and cybersecurity engineering skills.

The environment focuses on:

cloud security hardening
deception engineering
SSH attack monitoring
SIEM integration
incident detection and analysis
threat visualization
SOC workflows

The honeypot continuously collects real-world attack traffic from internet scanners, brute-force bots, and credential stuffing campaigns targeting exposed SSH services.

Architecture Overview

You can later add:

architecture diagram
network flow diagram
screenshots
detection dashboards
attack maps

Example flow:

Internet Attackers
        ↓
AWS EC2 Public IP
        ↓
Cowrie SSH Honeypot (Port 22)
        ↓
JSON Logs
        ↓
SIEM / Detection Platform
        ↓
Dashboards + Alerts + Analysis
Phase 1 — Cloud Honeypot Deployment & SSH Hardening
Objective

Build and harden a cloud-hosted SSH honeypot environment on AWS.

Key Concepts
AWS EC2 deployment
Linux server administration
SSH hardening
Security groups
Port separation
Honeypot deployment
Attack surface reduction
Principle of least privilege
Implemented
Deployed Ubuntu EC2 instance in AWS
Configured AWS security groups
Hardened SSH configuration
Disabled root SSH login
Moved legitimate SSH administration to port 2222
Deployed Cowrie honeypot on port 22
Configured restricted administrative access by source IP
Verified live internet scanning and attack traffic
Captured real-world SSH probe activity
Technologies
AWS EC2
Ubuntu Linux
OpenSSH
Cowrie
Python virtual environments
Authbind
Systemd
Skills Demonstrated
Cloud infrastructure management
Linux administration
Network security
SSH security architecture
Honeypot deployment
Cloud attack surface management
Phase 2 — Log Collection & Threat Telemetry
Objective

Centralize and structure honeypot attack data for analysis.

Planned Features
JSON log collection
Session tracking
Command logging
Attacker IP extraction
Credential attempt analysis
Geolocation enrichment
Threat intelligence enrichment
Technologies
Cowrie JSON logs
Python
GeoIP
Threat feeds
Log parsing
Skills Demonstrated
Security telemetry
Log analysis
Threat hunting
Attack pattern analysis
Python scripting
Phase 3 — SIEM Integration & Detection Engineering
Objective

Forward honeypot telemetry into a SIEM platform for SOC-style monitoring and alerting.

Planned Features
Centralized log ingestion
Real-time alerts
Detection rules
Brute-force detections
Dashboard creation
IOC tracking
MITRE ATT&CK mapping
Possible Platforms
Wazuh
ELK Stack
Splunk
Microsoft Sentinel
Skills Demonstrated
SIEM engineering
Detection engineering
SOC workflows
Threat monitoring
Alert triage
Phase 4 — Threat Visualization & Analytics
Objective

Visualize attacker activity and identify trends across collected telemetry.

Planned Features
Attack maps
Geographic visualization
Top attacker IPs
Most attempted usernames/passwords
Attack frequency trends
Session analytics
Brute-force statistics
Skills Demonstrated
Threat intelligence analysis
Security analytics
Dashboard design
Data visualization
Phase 5 — Advanced Cloud Security Engineering
Objective

Expand the lab into a more production-like cloud security environment.

Planned Features
Multi-honeypot deployment
VPC segmentation
IDS/IPS integration
Automated blocking
CloudWatch integration
Infrastructure as Code
Detection automation
Incident response workflows
Possible Technologies
Terraform
Suricata
Security Onion
AWS GuardDuty
Lambda
CloudWatch
Skills Demonstrated
Cloud security engineering
Infrastructure automation
Incident response
Network security
Detection automation
Real-World Problem Addressed

Internet-facing SSH services are continuously targeted by:

automated reconnaissance
brute-force attacks
credential stuffing
botnet scanning

Security researchers have observed that newly deployed cloud servers can receive SSH probing attempts within minutes of becoming publicly accessible.

This project demonstrates how deception technologies and centralized monitoring can improve visibility into attacker behavior while reducing exposure of legitimate administrative services.
