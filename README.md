# Network Intrusion Detection System (NIDS)

## Overview
This project demonstrates a basic Network Intrusion Detection System using Suricata on Windows. It monitors network traffic and generates alerts when traffic matches configured detection rules.

## Objective
The objective is to understand network monitoring, packet capture, custom detection rules, and security alert analysis.

## Tools & Technologies
- Suricata IDS
- Npcap
- Windows
- Custom Suricata rules
- ICMP / Ping for testing

## How It Works
1. Suricata monitors traffic on a selected network interface.
2. A custom rule checks for ICMP traffic.
3. Ping is used to generate test traffic.
4. Matching traffic triggers an alert.
5. Alerts are recorded in `fast.log`.

## Custom Detection Rule
```text
alert icmp any any -> any any (msg:"CodeAlpha NIDS - ICMP traffic detected"; sid:1000001; rev:1;)
```

This rule generates an alert when traffic matches the ICMP rule conditions.

## Testing
- Configured Suricata and a custom ICMP detection rule.
- Generated ICMP traffic using the ping command.
- Verified alerts in Suricata's `fast.log`.

## Project Structure
```text
Network-Intrusion-Detection-System/
├── rules/
│   └── local.rules
├── logs/
└── README.md
```

*The structure may vary depending on the local configuration. Do not upload raw logs or sensitive network details.*

## Limitations
This is a basic demonstration focused on ICMP traffic detection. An alert does not necessarily indicate a malicious attack. Additional rules and testing are required to detect other threats.

## Learning Outcomes
- Basic network traffic monitoring
- Packet capture concepts
- Suricata rule configuration
- Security alert and log analysis

## Author
Completed as part of the CodeAlpha Cyber Security Internship task.
