# windows-failed-login-detection
SOC/Blue Team home lab for detecting and investigating Windows failed login attempts using Event ID 4625, Event Viewer, and PowerShell.
# Windows Failed Login Detection Lab

## Project Overview

This cybersecurity home lab demonstrates how to identify and investigate failed Windows login attempts using Windows Event Viewer and PowerShell.

Windows records failed login attempts as Security Event ID 4625. Monitoring these events can help SOC analysts identify suspicious authentication activity, password attacks, and unauthorized access attempts.

## Objectives

- Generate a failed Windows login attempt
- Locate Event ID 4625 in Windows Event Viewer
- Examine important information associated with the failed login
- Use PowerShell to search Windows Security logs
- Understand how SOC analysts investigate authentication failures

## Tools Used

- Windows
- Windows Event Viewer
- PowerShell
- Windows Security Logs

## Step 1 – Generate a Failed Login

I intentionally attempted to log in using an incorrect password in my Windows lab environment.

This generated a failed authentication event in the Windows Security log.

## Step 2 – Open Event Viewer

I opened:

Event Viewer → Windows Logs → Security

I then searched the Security log for:

Event ID: 4625

Event ID 4625 indicates that an account failed to log on.

## Step 3 – Investigate the Event

I reviewed information contained in the event, including:

- Date and time
- Account name
- Logon type
- Failure reason
- Source information
- Process information

These details can help a SOC analyst determine whether the failed login was caused by a normal user mistake or potentially suspicious activity.

## Step 4 – PowerShell Detection

I also used PowerShell to search for failed login events.

The PowerShell script used for this investigation is available here:

`scripts/failed-login-detection.ps1`

## Screenshots

### Windows Security Log

Screenshot showing the Windows Security log and failed login event.

` screenshots/01-event-viewer-security-log.png `

### Event ID 4625

Screenshot showing the details associated with Event ID 4625.

` screenshots/02-event-id-4625.png `

### PowerShell Detection

Screenshot showing the PowerShell query results.

` screenshots/03-powershell-results.png `

## What I Learned

This lab helped me understand how Windows records authentication failures and how security analysts can investigate failed login attempts.

I also gained hands-on experience using Windows Event Viewer and PowerShell to identify security events.

Repeated failed login attempts can be an indicator that requires further investigation, especially when they occur from unusual accounts, systems, or sources.

## Skills Demonstrated

- SOC Analysis
- Windows Event Log Analysis
- Authentication Monitoring
- PowerShell
- Security Event Investigation
- Incident Triage
- Windows Security
