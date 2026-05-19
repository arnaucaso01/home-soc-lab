# home-soc-lab
Building a home SOC lab with Wazuh, Sysmon and real attack simulations

A hands-on Security Operations Center (SOC) home lab designed to simulate real-world cyber attacks, generate security telemetry, and improve threat detection and incident response skills.

## Project Goals
- Build a realistic SOC environment
- Collect and analyze Windows and Linux security logs
- Detect malicious activity using SIEM rules
- Simulate real-world attack scenarios
- Improve incident investigation skills
  
## Lab Architecture
| Machine | Role |
|---------|------|
| Kali Linux | Attacker |
| Windows 10 | Victim |
| Ubuntu Server | Wazuh SIEM |

## Tools Used
- Wazuh
- Sysmon
- VirtualBox
- Kali Linux
- Ubuntu Server
- Windows Event Viewer
- Nmap

## Current Attack Simulations

- [ ] Port Scanning Detection
- [ ] Brute Force Detection
- [ ] Suspicious PowerShell Execution
- [ ] Privilege Escalation Attempts

## Screenshots

The Wazuh dashboard with the Windows agent active and showing its details.

![Wazuh active agent](screenshots/wazuh-agents-active.png)

Sysmon events in the Windows Event Viewer, mainly process creation.

![Sysmon logs](screenshots/sysmon-operational-logs.png)

Running an nmap TCP connect scan from Kali to the Windows machine.

![Nmap scan](screenshots/kali-nmap-scan.png)

Windows Security event 5156 where the Kali IP appears in the log.

![Windows 5156](screenshots/windows-5156-kali.png)

A custom alert in Wazuh for port scanning activity, mapped to MITRE T1046.

![Wazuh alerts](screenshots/wazuh-dashboard-alerts.png)

## MITRE ATT&CK Mapping

This lab will include detections mapped to:

- T1059 – Command and Scripting Interpreter
- T1110 – Brute Force
- T1046 – Network Service Discovery
