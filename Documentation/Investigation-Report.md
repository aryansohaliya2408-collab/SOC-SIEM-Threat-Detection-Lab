# SOC SIEM Threat Detection and Incident Investigation Report

## 1. Project Overview

This project is a hands-on Security Operations Center (SOC) home lab built using Wazuh SIEM. The objective was to monitor Windows endpoint security events, detect authentication failures, and investigate security alerts.

## 2. Lab Environment

| Component | Technology |
|---|---|
| SIEM | Wazuh |
| Server OS | Ubuntu Linux |
| Endpoint OS | Windows 11 |
| Container Platform | Docker |
| Virtualization | Oracle VirtualBox |
| Agent | Wazuh Windows Agent |

## 3. Project Objectives

- Deploy and configure Wazuh SIEM.
- Connect a Windows endpoint to the Wazuh manager.
- Monitor Windows security events.
- Detect failed login attempts.
- Investigate authentication failure alerts.
- Understand security event details and alert severity.

## 4. Implementation

1. Installed Wazuh SIEM on an Ubuntu virtual machine.
2. Configured the Wazuh manager and dashboard.
3. Installed and connected the Wazuh agent on Windows 11.
4. Verified that the Windows agent was active.
5. Generated test failed-login events.
6. Monitored the events in the Wazuh dashboard.

## 5. Security Incident Investigation

**Event ID:** 4625

**Event Description:** An account failed to log on.

**Wazuh Rule ID:** 60122

**Rule Level:** 5

**Alert Description:** Logon Failure - Unknown user or bad password.

**Agent Name:** DESKTOP-TGPRRHB

**Agent ID:** 001

**Logon Type:** 2 (Interactive logon)

**Status:** 0xc000006d

**Substatus:** 0xc000006a

### Investigation Findings

- Wazuh successfully collected Windows authentication failure events.
- The dashboard displayed 18 authentication failure alerts in the selected search period.
- Wazuh generated alerts using rule ID 60122.
- Event details showed unsuccessful authentication.
- The investigation demonstrated how a SOC analyst can review endpoint security logs and investigate failed login activity.

## 6. Security Analysis

Repeated failed login attempts can indicate possible password guessing or unauthorized access attempts. However, failed logins alone do not confirm an attack.

A SOC analyst should investigate:
- Number and frequency of failed attempts.
- Target username.
- Source IP address.
- Event timestamps.
- Whether a successful login followed the failures.

## 7. Skills Demonstrated

- SIEM deployment and configuration.
- Windows endpoint monitoring.
- Security event log analysis.
- Authentication failure investigation.
- Wazuh alert monitoring.
- Basic incident investigation.

## 8. Conclusion

This project provided practical experience with Wazuh SIEM, Windows endpoint monitoring, security event analysis, and failed-login investigation. It helped develop foundational skills relevant to a SOC Analyst Level 1 role.

## 9. Evidence

Screenshots of the Wazuh dashboard, active Windows agent, Event ID 4625, security alerts, and investigation details are available in the Screenshots folder.

## Author

Aryan Sohaliya  
B.Tech Cyber Security Student  
Aspiring SOC Analyst L1
