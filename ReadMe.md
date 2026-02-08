# Windows Endpoint & Authentication Monitoring (SOC Lab)

## Overview
This project demonstrates hands-on SOC analyst skills by simulating authentication attacks and analyzing endpoint telemetry using Windows Security logs and Sysmon. The lab replicates real-world investigation workflows including detection, triage, and event correlation.

## Objectives
- Generate security telemetry from endpoint and authentication activity  
- Detect failed login attempts and suspicious user actions  
- Analyze Windows and Sysmon logs  
- Perform SOC-style investigation and validation  

## Tools Used
- Windows 10 Virtual Machine  
- Sysmon  
- Windows Event Viewer  

## Attack Simulation
- Created local test account using:
- net user fakeuser fakepass123 /add
- Generated multiple failed login attempts to trigger security events  
- Produced authentication telemetry for analysis  

## Detection & Analysis
### Authentication Monitoring
- Identified failed logins using Event ID **4625**
- Reviewed account name, failure reason, and logon type
- Compared against successful login events (4624)

### Endpoint Telemetry
- Reviewed Sysmon Operational logs
- Analyzed process execution metadata including:
  - Image paths
  - Command-line arguments
  - User context
  - Event IDs

## Investigation Outcome
Analysis confirmed repeated authentication failures targeting a local account with no successful compromise events observed. Endpoint telemetry validated normal system process behavior and provided visibility into execution context.

## Skills Demonstrated
- Security log analysis  
- Threat detection  
- SOC triage workflow  
- Event correlation  
- Endpoint monitoring fundamentals  

## Screenshots

| # | Screenshot | Description |
|---|------------|-------------|
| 1 | 01_sysmon_install.png | Sysmon installed via PowerShell |
| 2 | 02_sysmon_logs.png | Sysmon Operational log list |
| 3 | 03_sysmon_event_details.png | Sysmon event details (Image, CommandLine, User) |
| 4 | 04_attack_command.png | Created local fakeuser account |
| 5 | 05_failed_logins.png | Failed login events (4625) |
| 6 | 06_failed_login_details.png | Failed login event details |
| 7 | 07_successful_logins.png | Successful login events (4624) |
| 8 | 08_sysmon_logs_repeat.png | Sysmon log list after activity |
| 9 | 09_sysmon_event_details_repeat.png | Another Sysmon event detail |
