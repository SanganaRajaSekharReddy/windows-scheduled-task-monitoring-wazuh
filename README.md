# Windows Scheduled Task Monitoring and Investigation Using Wazuh

## Project Overview

This project demonstrates how to monitor and investigate Windows Scheduled Task creation events using Wazuh SIEM.

Scheduled Tasks can be used by administrators to automate activities. However, attackers may also abuse them to maintain persistence on a compromised Windows system.

In this lab, I created test scheduled tasks, enabled Windows auditing, and investigated Event ID 4698 using Wazuh.

## Objectives

- Monitor Windows Scheduled Task creation.
- Enable Windows Security auditing.
- Identify Event ID 4698.
- Collect Windows Security events using Wazuh Agent.
- Investigate security events in Wazuh Dashboard.
- Understand scheduled task abuse as a persistence technique.

## Lab Environment

| Component | Details |
|---|---|
| SIEM | Wazuh |
| Server OS | Ubuntu |
| Endpoint OS | Windows |
| Virtualization | Oracle VirtualBox |
| Log Source | Windows Security |
| Event ID | 4698 |

## Tools Used

- Wazuh SIEM
- Windows Event Viewer
- Windows PowerShell
- Oracle VirtualBox

## Lab Implementation

### Step 1: Create a Scheduled Task

Created test scheduled tasks in Windows using PowerShell.

### Step 2: Enable Auditing

Enabled auditing for Other Object Access Events to record scheduled task creation activity.

### Step 3: Identify Windows Event ID

Verified Event ID 4698 in Windows Security logs.

**Event ID 4698:** A scheduled task was created.

### Step 4: Configure Wazuh Agent

Configured the Windows Wazuh Agent to collect Windows Security events and verified that the agent was active.

### Step 5: Investigate Events

Searched for Event ID 4698 in Wazuh using the query:

`data.win.system.eventID:4698`

Investigated the available event details, including event information and scheduled task activity.

## Investigation Findings

- Windows generated Event ID 4698 when a scheduled task was created.
- Wazuh collected Windows Security events from the endpoint.
- The scheduled task creation event was investigated in Wazuh.
- Scheduled task creation can be a legitimate administrative activity or a possible persistence technique.

## Screenshots

Screenshots of the lab setup and investigation are available in the `screenshots` folder.

## Skills Demonstrated

- SIEM Monitoring
- Windows Event Log Analysis
- Wazuh Agent Configuration
- Security Event Investigation
- PowerShell
- Basic Threat Detection
- Understanding Persistence Techniques

## Learning Outcome

I learned how Windows scheduled task creation events are generated, collected, and investigated using Wazuh SIEM.

## Disclaimer

This project was performed in my own virtual lab for educational and defensive cybersecurity learning purposes.

