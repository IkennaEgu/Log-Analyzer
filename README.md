# Log-Analyzer
A Python-based security tool designed to analyse Linux authentication logs (auth.log) and extract security-relevant events, including:

User account creation
User account deletion
Password changes
User switching (su)
Sudo command execution
Failed privilege escalation attempts

The tool was developed to improve understanding of Linux logging, security monitoring, and incident investigation techniques commonly used by Security Operations Centre (SOC) analysts and system administrators.

Features
User Account Monitoring:
Identifies newly created user accounts from auth.log.

Account Deletion Tracking:
Detects deleted user accounts and records associated timestamps.

Password Change Monitoring:
Extracts password modification events.

User Switching Detection:
Tracks su sessions to identify privilege transitions between accounts.

Sudo Activity Monitoring:
Displays users executing privileged commands.

Failed Privilege Escalation Detection:
Flags users attempting to execute sudo commands without appropriate permissions.

Technologies Used
Python 3
Linux Authentication Logs (/var/log/auth.log)
AWK
Bash/Linux Command Line

Example Output
Newly added users:
Jun useradd newuser

Deleted users:
Jun delete user testuser

Password changes:
Jun password changed for user analyst

Sudo Usage:
ubuntu apt update

Failed Sudo Attempts:
ALERT! john is not in sudoers


Security Use Cases
Insider Threat Monitoring
Track creation and deletion of user accounts.
Privilege Escalation Detection
Identify suspicious sudo and su activity.
Incident Response
Review authentication events during security investigations.
System Auditing
Provide administrators with visibility into authentication-related changes.

Future Improvements
Replace os.system() calls with Python's subprocess module.
Parse logs directly using Python instead of AWK.
Export results to CSV and JSON.
Add regular expression support.
Create a command-line interface with arguments.
Generate alerts for suspicious activities.
Integrate with Splunk or a SIEM platform.

This project was developed in a controlled lab environment to improve understanding of Linux authentication logs and security monitoring techniques.
