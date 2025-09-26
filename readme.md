  Setup and Use a Firewall on Windows
  
  Objective

The aim of this task was to configure and test firewall rules on a Windows 10 machine. I explored how to allow and block traffic, documented each step, and tested the rules for verification.

Steps Followed
Step 1: Opening Firewall Settings

Pressed Win + R, typed wf.msc, and pressed Enter.

This opened Windows Defender Firewall with Advanced Security.

Step 2: Checking Existing Rules

Selected Inbound Rules from the left panel.

Noted down the default rules already present (Remote Desktop, File Sharing, etc.).

Also checked using PowerShell to view all rules in list format.

Step 3: Blocking Telnet (Port 23)

Created a New Rule under Inbound Rules.

Selected Port, chose TCP, and entered 23.

Chose Block the connection and applied it to all profiles (Domain, Private, Public).

Named the rule Block Telnet Port 23.

Step 4: Testing the Rule

Tried connecting with telnet localhost 23.

The connection failed, confirming the rule was successfully applied.

Step 5: Allowing SSH (Port 22)

Again created a New Rule.

Selected Port, chose TCP, and entered 22.

Chose Allow the connection and applied it to all profiles.

Named the rule Allow SSH Port 22.

Step 6: Removing the Test Rule

Located the rule Block Telnet Port 23.

Deleted it to restore the system to its original state.

Step 7: Documentation with Screenshots

Captured the following screenshots:

Firewall Advanced Settings window.

Rule creation process.

Telnet blocked test.

Allowed SSH rule.

Firewall restored to original state.

 Summary

A firewall filters traffic to improve system security.

Inbound rules manage incoming traffic, while outbound rules manage outgoing traffic.

Blocking Telnet (Port 23) is important because it is outdated and insecure.

Allowing SSH (Port 22) ensures secure remote access.

Windows Firewall can be configured through both GUI and PowerShell.

 Deliverables

README.md (this file).


Screenshots folder with proof of steps.

