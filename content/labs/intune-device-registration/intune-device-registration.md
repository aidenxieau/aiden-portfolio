---
title: "Troubleshooting Intune Device Registration"
date: 2026-06-07
draft: false
tags:
  - Microsoft Intune
  - Entra ID
  - Windows 10
categories:
  - Troubleshooting
---

## Objective

The goal of this lab was to enrol a Windows 10 device into Microsoft Intune and associate it with the correct user.

## Environment

- Windows 10
- Microsoft Entra ID
- Microsoft Intune
- Microsoft 365 Business Premium

## Problem

The device appeared in Microsoft Entra ID, but it was not displayed correctly in Microsoft Intune.
![intune problem](./imgae/intune_problem.png)
## Investigation

steps I checked:

S1. The user's Microsoft 365 licence
![intune problem](./imgae/check_licence.png)

S2. The device status in Microsoft Entra ID
![intune problem](./imgae/intune_admin_info.png)

S3. The Intune automatic enrolment scope
![intune problem](./imgae/check-MDM-scope.png)

S4. The user and device association run dsregcmd /status
```
      AzureAdJoined : NO
      EnterpriseJoined : NO
      WorkplaceJoined : YES

      WorkplaceSettingsUrl :
```      

## Resolution

After checking the enrolment settings and reconnecting the work account, the device successfully appeared in Microsoft Intune.

## Verification

The device was visible in both Microsoft Entra ID and Microsoft Intune.

## Troubleshooting Workflow
```text
Check Device State
        ↓
Check License
        ↓
Check MDM User Scope
        ↓
Run dsregcmd /status
        ↓
Verify MDM Discovery
        ↓
Perform Enrollment
        ↓
Verify Intune Management State
```