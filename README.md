# Using Wazuh and Sysmon for Cyber Defense

## Overview
This repository contains a detailed lab write-up on using Wazuh, an open-source security monitoring and incident response tool, in conjunction with Sysmon, to investigate a security breach on a compromised system. The lab demonstrates how to identify attack vectors, monitor system activities, and respond to threats effectively.

## Table of Contents
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Lab Environment](#lab-environment)
- [Tools and Technologies Used](#tools-and-technologies-used)
- [Step-by-Step Process](#step-by-step-process)
- [Results and Analysis](#results-and-analysis)
- [Challenges Faced](#challenges-faced)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction
In this lab, Wazuh is utilized to analyze a system intrusion, identify how the attacker gained initial access, and uncover malicious activities such as the creation of scheduled tasks, new user accounts, and credential dumping.

## Objectives
- Identify how the attacker gained initial access to the system.
- Determine the scheduled tasks created by the attacker.
- Retrieve credentials of newly created user accounts.
- Discover the executable used for credential dumping.
- Extract credentials that were leaked during the attack.

## Lab Environment
- **Platform**: TryHackMe (Monday Monitor Challenge)
- **Wazuh Manager**: Accessed through a web browser
- **Agents**: Two Windows Server 2019 machines

## Tools and Technologies Used
- **Wazuh**: Open-source security monitoring and incident response tool.
- **Sysmon**: Windows system service and device driver.
- **CyberChef**: Tool for decoding encoded data.

## Step-by-Step Process
1. **Initial Access Identification**: Analyzing logs to identify the source of the initial compromise.
2. **Scheduled Task Analysis**: Investigating scheduled tasks created by the attacker.
3. **Decoding Commands**: Using CyberChef to decode encoded commands.
4. **Discovering New Account Credentials**: Analyzing events to identify newly created accounts and their credentials.
5. **Executable Analysis**: Identifying the executable used for credential dumping.

For a detailed step-by-step process, please refer to the [full lab write-up](link-to-full-write-up).

## Results and Analysis
- Identified the initial access vector through a suspicious file execution.
- Discovered malicious scheduled tasks created for persistent command and control (C2) activity.
- Retrieved credentials of a newly created account used for maintaining access.
- Found the executable (`memotech.exe`) used for credential dumping, which is a disguised version of Mimikatz.

## Challenges Faced
- Effectively filtering commands and understanding log data.
- Decoding Base64 encoded commands.
- Identifying disguised tools and their usage.

## Conclusion
This lab exercise highlighted the importance of effective monitoring and analysis using tools like Wazuh and Sysmon. By identifying attack vectors, detecting malicious activities, and understanding attack patterns, we enhance our capabilities in threat hunting and incident response.

## References
- [Wazuh Documentation](https://documentation.wazuh.com)
- [TryHackMe Monday Monitor Challenge](https://tryhackme.com)
- [CyberChef Tool](https://gchq.github.io/CyberChef/)
- [Microsoft Docs - Command-Line Reference](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands)
- [MITRE ATT&CK Framework](https://attack.mitre.org)

