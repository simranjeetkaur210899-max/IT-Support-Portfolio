# Password Reset and Account Unlock

**Audience:** Help desk technician
**Difficulty:** Easy
**Time to fix:** about 5 minutes
**Last tested:** [date], Windows Server 2022 / Windows 11, domain lab.local

## Problem

A user says they can't log in. Either they forgot their password, or they typed it wrong too many times and the account is locked ("Your account has been locked out...").

## Quick checks (ask the user first)

1. Is it a forgotten password, or did they type it correctly and it still fails?
2. Is Caps Lock on? Are they using the right keyboard layout?
3. Did their password recently expire or change?
4. Are they logging in to the right domain (`LAB\username`)?

## Likely causes

- Forgotten or expired password
- Account locked out after too many failed attempts
- Old saved password on a phone, mapped drive, or another computer repeatedly retrying (causes repeated lockouts)
- Account disabled (for example, the employee left or is on leave)

## Steps to fix

**Step 0: Verify identity.** Before changing anything, confirm who you are talking to. Ask for their employee ID and manager's name, or follow your company's verification process. Never reset a password for someone you haven't verified.

1. On the domain controller or an admin workstation, open **Active Directory Users and Computers** (Start menu, then Windows Administrative Tools).
2. Find the user: right-click the domain, choose **Find**, and search by name or username.
3. Right-click the user and open **Properties**, then the **Account** tab.
4. Check the account status:
   - If it says the account is locked out, tick **Unlock account** and click **OK**.
   - If **Account is disabled** is shown, do not enable it yourself. Escalate (see below).
5. To reset the password: right-click the user, choose **Reset Password**.
6. Enter a temporary password that follows the password policy.
7. Tick **User must change password at next logon**. Leave **Unlock the user's account** ticked if it's offered.
8. Click **OK**.
9. Give the user the temporary password through a safe channel (by phone, never by email or chat).

## How to confirm it's fixed

- The user logs in with the temporary password and is prompted to choose a new one.
- Ask them to confirm they can open email and their network drive.
- Close the ticket only after they confirm.

## When to escalate

Escalate to Tier 2 or the sysadmin if:

- The account is **disabled** (needs approval from HR or the manager).
- The account **locks again within minutes**. Something is retrying an old password, and you need to find the source.
- You can't verify the user's identity.
- You see signs of a security issue, such as login attempts at odd hours or from unknown locations.

In the escalation note, include: username, time of the lockout, what you tried, and what the user was doing when it began.

## Notes

- A reset and an unlock are different things. Unlocking keeps the current password; resetting replaces it.
- Repeated lockouts are almost always an old saved password on a phone or a mapped drive. Ask the user what other devices they use.
