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
See `/screenshots` folder for evidence of:
- Sysmon installation and logs  
- Failed login events  
- Successful login events  
- Event details
