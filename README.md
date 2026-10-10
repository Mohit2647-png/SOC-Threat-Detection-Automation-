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

This project implements network threat detection using Splunk SIEM, Suricata, and log analysis.

### 1. SSH Brute-Force Detection
- Detects repeated failed SSH login attempts.
- Analyzes Ubuntu authentication logs using Splunk Search Processing Language (SPL).
- Helps identify potential unauthorized access attempts.

### 2. SMB Traffic Detection
- Monitors SMB (Server Message Block) network traffic.
- Helps investigate potentially suspicious file-sharing activity.
- Supports network security monitoring and threat investigation.

### 3. HTTP Beaconing Detection
- Identifies repeated HTTP connections that may occur at regular intervals.
- Helps investigate potential command-and-control (C2) communication.
- Uses network traffic data and Splunk searches to identify suspicious patterns.

### 4. Nmap Port Scan Detection
- Detects potential network reconnaissance by identifying connections to multiple destination ports.
- Analyzes source IP addresses, destination IP addresses, and port activity.
- Helps identify hosts that may be scanning systems for exposed services.

## AI-Powered SOC Alert Analysis

Integrated n8n Cloud with Splunk alerts to automate initial security alert analysis using an AI Agent.

**Workflow:**

`Splunk Alert → Webhook → Edit Fields → AI Agent → Email Report`

### Automated Analysis Features
- Receives Splunk alert data through a webhook.
- Extracts alert details, severity, and available IP addresses.
- Uses an AI Agent to analyze the alert and summarize the evidence.
- Generates a report with a risk assessment and recommended investigation steps.
- Sends the analysis to email for review by a security analyst.

## Tools and Technologies

- **Splunk SIEM** — log analysis, SPL queries, saved searches, and alerts.
- **Suricata IDS** — network traffic monitoring and event generation.
- **Ubuntu Linux** — log collection and Universal Forwarder.
- **Kali Linux** — controlled security testing in the lab.
- **Windows** — Splunk receiving server and security lab environment.
- **n8n Cloud** — workflow automation.
- **AI Agent** — initial alert analysis and report generation.

## Skills Demonstrated

- SIEM configuration and alert management
- SPL query development
- Network traffic analysis
- SSH authentication monitoring
- SMB traffic monitoring
- HTTP beaconing analysis
- Network reconnaissance detection
- Security alert automation
- AI-assisted SOC investigation
- Email-based alert reporting

## Security Note

This project was developed for educational purposes in a controlled virtual lab. AI-generated reports support initial triage and should be reviewed by a human analyst. No automated IP blocking or other destructive response actions are performed.
