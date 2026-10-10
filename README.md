# SOC-Threat-Detection-Automation-
SOC home lab using Splunk, Suricata, and n8n AI automation for security alert analysis
# SOC Network Threat Detection Lab with AI Automation

## Overview

This project demonstrates a hands-on Security Operations Center (SOC) lab built using Splunk, Suricata, Ubuntu, Kali Linux, and Windows. It focuses on network threat detection, log monitoring, security alerting, and AI-powered security alert analysis using n8n.

The project also integrates Splunk alerts with an n8n AI workflow that analyzes security events and sends an email report with findings and recommended investigation steps.

## Project Objectives

- Configure a SIEM environment using Splunk.
- Collect and analyze network traffic events using Suricata.
- Forward Ubuntu authentication logs to Splunk.
- Develop SPL searches for detecting suspicious activity.
- Configure saved alerts for security detections.
- Automate alert analysis using an n8n AI Agent.
- Generate email reports to support SOC investigation.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Splunk Enterprise | SIEM, log analysis, SPL searches, and alerts |
| Suricata | Network intrusion detection and EVE JSON logging |
| Ubuntu Linux | Log collection and Splunk Universal Forwarder |
| Kali Linux | Controlled security testing |
| Windows | Splunk receiving and monitoring environment |
| n8n Cloud | Workflow automation |
| AI Agent | Security alert analysis and investigation recommendations |

## Lab Architecture

1. Kali Linux generates controlled test traffic.
2. Suricata monitors network traffic and generates security events.
3. Ubuntu authentication logs provide host-level security events.
4. The Splunk Universal Forwarder sends selected logs to Splunk Enterprise.
5. Splunk searches analyze events and trigger configured alerts.
6. A webhook sends alert data to n8n.
7. The n8n AI Agent analyzes the alert and recommends investigation steps.
8. The workflow sends an email report containing the analysis.

## Detection Scenarios

### 1. Nmap Port Scan Detection
Identifies potential network reconnaissance by analyzing connection activity and the number of destination ports contacted by a source IP.

### 2. SSH Brute-Force Detection
Analyzes Ubuntu authentication logs to identify repeated failed SSH login attempts.


### 3. DNS Anomaly Detection
Uses available DNS telemetry to investigate unusual DNS activity that may indicate suspicious
