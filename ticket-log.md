# Practice Ticket Log

Priority guide:
- **P1 Critical:** many users down or a business-critical system is down
- **P2 High:** one user fully blocked from working
- **P3 Medium:** one user affected, workaround exists
- **P4 Low:** question or request, no urgency

| ID | Date | Category | Priority | Summary | Status |
|---|---|---|---|---|---|
| 001 | [date] | Account | P2 | User locked out of account | Resolved |
| 002 | | | | | |
| 003 | | | | | |

---

## Ticket 001: User locked out of account

- **Reported by:** [fictional user, e.g., Jordan Lee, Sales]
- **Date / time:** [date, time]
- **Category:** Account access
- **Priority:** P2 (user cannot work)

**Description:** User reports "Your account has been locked out" when logging in after returning from vacation.

**Steps taken:**
1. Verified identity with employee ID and manager name.
2. Opened Active Directory Users and Computers and found the account.
3. Confirmed the account was locked out.
4. Unlocked the account, then reset the password with "must change at next logon" ticked.
5. Gave the temporary password by phone.

**Resolution:** User logged in and set a new password. Confirmed email and network drive work.

**Root cause:** Several failed attempts with an old password after the vacation.

**Time spent:** 6 minutes
**Linked guide:** [Password Reset and Account Unlock](../guides/01-password-reset-and-account-unlock.md)

---

## Ticket template

## Ticket 00X: [Title]

- **Reported by:**
- **Date / time:**
- **Category:**
- **Priority:**

**Description:**

**Steps taken:**
1.

**Resolution:**

**Root cause:**

**Time spent:**
**Linked guide:**
