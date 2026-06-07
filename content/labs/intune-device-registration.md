---
title: "Troubleshooting Intune Device Registration"
date: 2026-06-07
draft: false
tags:
  - Microsoft Intune
  - Entra ID
  - Windows 11
categories:
  - Troubleshooting
---

## Objective

The goal of this lab was to enrol a Windows 11 device into Microsoft Intune and associate it with the correct user.

## Environment

- Windows 11
- Microsoft Entra ID
- Microsoft Intune
- Microsoft 365 Business Premium

## Problem

The device appeared in Microsoft Entra ID, but it was not displayed correctly in Microsoft Intune.

## Investigation

I checked:

1. The user's Microsoft 365 licence
2. The device status in Microsoft Entra ID
3. The Intune automatic enrolment scope
4. The user and device association
5. The Windows work or school account

## Resolution

After checking the enrolment settings and reconnecting the work account, the device successfully appeared in Microsoft Intune.

## Verification

The device was visible in both Microsoft Entra ID and Microsoft Intune.

## What I Learned

A device appearing in Microsoft Entra ID does not always mean that it has successfully enrolled in Microsoft Intune.