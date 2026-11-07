# Windows Endpoint Threat Investigation

## 1. Investigation Overview

**Scenario:** Simulated suspicious activity on a Windows endpoint.

**Hostname:** WIN-CLIENT01

**Account under investigation:** j.smith

**Investigation date:** 7 November 2026

**Objective:** Investigate suspicious authentication activity and PowerShell commands to identify potential endpoint threats.

## 2. Initial Findings

The simulated Windows security logs revealed:

- Three consecutive failed login attempts for j.smith.
- A successful login shortly after the failed attempts.
- The login attempts originated from the same IP address: 192.0.2.45.
- Command Prompt and PowerShell were subsequently launched.
- PowerShell commands included Get-LocalGroupMember and Get-Process.
- The whoami command was executed to identify the current user context.

## 3. Relevant Windows Event IDs

| Event ID | Description |
|---|---|
| 4625 | Failed logon attempt |
| 4624 | Successful logon |
| 4688 | Process creation |
| 4104 | PowerShell script block logging |

## 4. Potential Security Concerns

The sequence of failed logins followed by a successful login could indicate password guessing or unauthorised access.

The subsequent PowerShell activity may indicate system discovery or reconnaissance.

However, these activities can also occur during legitimate administration and require further investigation.

## 5. Recommended Investigation Steps

- Verify the login activity with the account owner.
- Review additional Windows authentication logs.
- Investigate the source IP address.
- Examine PowerShell command history and script block logs.
- Determine whether the commands were authorised.
- Check for unusual account or privilege changes.
- Escalate confirmed suspicious activity to the appropriate security team.

## 6. Conclusion

The simulated logs show potentially suspicious authentication and PowerShell activity requiring further investigation.

**Final assessment:** Suspicious endpoint activity – further investigation required.

## 7. Investigation Limitations

This exercise uses fictional Windows security events. No live endpoint, real user account or production security logs were involved.

The available evidence is insufficient to confirm a security compromise.
