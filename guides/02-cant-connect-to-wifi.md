# Can't Connect to Wifi

**Audience:** [End user / Help desk technician]
**Difficulty:** [Easy / Medium / Hard]
**Time to fix:** [about X minutes]
**Last tested:** [date, and on which OS version]

## Problem

User's laptop shows no networks, or shows "No internet" or "Can't connect to this network"

## Quick checks 
- Is airplane mode on, or the Wi-Fi switch off?
- Do other devices connect to the same Wi-Fi?
- Did the user recently change their Wi-Fi password?
- Is the problem only at one location?

## Likely causes
- Wi-Fi turned off, wrong or changed password , stale saved connection, the adapter stuck, router/access point problem
  
## Steps to fix
1. Turn airplane mode off and make sure Wi-Fi is on.
2. Turn Wi-Fi off and on again.
3. Click the network, choose Forget, then reconnect and re-enter the password.
4. Restart the computer.
5. Open Command Prompt as administrator, run ipconfig /release, then ipconfig /renew, then ipconfig /flushdns.
6. Open Device Manager, find the Wi-Fi adapter under Network adapters, right-click it, and choose Disable device, then Enable device.


## How to confirm it's fixed

the user can open a website and reach their email

## When to escalate

Other users are affected too (it may be the router or access point), the Wi-Fi adapter doesn’t appear in Device Manager, or the computer connects but gets an address starting with 169.254 (a DHCP problem).

