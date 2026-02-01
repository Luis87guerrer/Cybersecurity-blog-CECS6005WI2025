---
layout: page
title: Incident Response Plan
permalink: /incident-response/
---

# Incident Response Plan (IRP): Your “calm brain” during a cyber incident

If cybersecurity had one rule, it would be this: **you don’t get to choose when an incident happens**—only how prepared you are when it does. That’s exactly what an **Incident Response Plan (IRP)** is for.

An **IRP** is a written, approved plan that tells an organization how to **prepare for**, **detect**, **respond to**, and **recover from** incidents (like ransomware, account compromise, data loss, or major outages). The goal isn’t to be perfect. The goal is to be **fast, organized, and consistent** when everything is stressful and time-sensitive.

## Why an IRP matters more than “good tools”
A lot of teams invest in security tools first (EDR, SIEM, firewalls) and only later think about incident response. But in a real incident, the biggest problems usually aren’t technical—they’re operational:

- Who is in charge right now?
- Who is allowed to disconnect systems?
- Who calls legal, leadership, or vendors?
- What do we tell employees or customers (and what should we NOT say yet)?
- What evidence do we preserve?

Without a plan, people hesitate, argue, or duplicate work—and minutes turn into hours. A good IRP reduces chaos by making roles and steps clear *before* the incident.

## What an IRP actually covers (the big picture)
Most incident response flows through the same “lifecycle.” Think of it like a loop:

### 1) Preparation
Preparation is where incident response succeeds or fails. This includes:
- Defining an incident response team and who leads it
- Training staff on how to report suspicious activity quickly
- Maintaining contact lists and escalation paths (including after-hours)
- Ensuring logs and monitoring exist (so you can investigate)
- Running tabletop exercises to practice decisions and communication

Preparation also includes “boring but critical” items like having offline access to key phone numbers and procedures in case email or chat is down.

### 2) Detection and analysis
This is where you answer: **Is this real? How bad is it? What is affected?**
You gather facts, confirm scope, and set severity so the response matches the impact. The earlier you confirm scope, the faster you can contain damage.

### 3) Containment
Containment is the “stop the bleeding” phase. It usually has two layers:
- **Short-term containment:** isolate affected devices, disable compromised accounts, block malicious domains/IPs.
- **Long-term containment:** segment networks, increase monitoring, rotate credentials, and patch the root weakness.

Containment decisions are where planning matters. Disconnecting a server can stop spread—but it can also break critical operations. The IRP gives decision-makers a safer path under pressure.

### 4) Eradication
Eradication means removing the cause:
- deleting malware or persistence mechanisms
- fixing the vulnerable service or misconfiguration
- removing unauthorized accounts/access
- closing the path the attacker used

### 5) Recovery
Recovery means restoring systems safely and watching for reinfection:
- restore from clean backups (if applicable)
- validate integrity (don’t restore infected data)
- monitor carefully after restoration
- gradually return to normal operations

### 6) Post-incident review (lessons learned)
This is the “how we get stronger” phase:
- What failed (process + control)?
- What worked well?
- What should be automated or documented better?
- What policy changes or training are needed?
- What metrics improved or got worse?

If you skip this step, the same incident pattern will happen again.

## Communication: the part that can destroy trust fast
Incidents aren’t only technical—they’re reputational. Your IRP should define:
- Who communicates with leadership
- Who communicates externally (if needed)
- What communication tools to use if normal tools are down
- How to keep messages consistent (one voice, not 10 rumors)

Even internally, communication matters. Employees will hear something. The question is whether they hear it from a controlled update… or a hallway rumor.

## Evidence and documentation (don’t lose the story)
A strong IRP emphasizes documenting actions and preserving evidence:
- timelines (what happened when)
- indicators of compromise
- systems affected
- actions taken (and who approved them)

This helps with recovery, legal needs, and prevention later.

## Real-world example: “One phishing click” scenario
Imagine an employee enters credentials into a fake login page. Minutes later:
- unusual logins appear from a new location
- the attacker starts forwarding email rules
- the attacker requests a wire transfer or tries password resets

With an IRP, the team knows the play:
1) confirm compromise via logs and user report  
2) disable the account + force password reset  
3) revoke sessions/tokens, remove forwarding rules  
4) check for lateral movement (other accounts, MFA changes)  
5) document and notify the right stakeholders  

Without an IRP, teams often waste time debating whether it’s serious—until money or data is gone.

## Common mistakes (and how to avoid them)
- **Plan exists but no one knows it:** train and run exercises.
- **No clear incident leader:** assign one role responsible for coordination.
- **No decision rules:** define what triggers containment actions.
- **No offline access:** assume email/chat may be unavailable.
- **No post-incident improvements:** treat incidents as learning events.

## References
- CISA — Incident Response Plan (IRP) Basics: https://www.cisa.gov/resources-tools/resources/incident-response-plan-irp-basics  
- Cisco — What Is an Incident Response Plan for IT?: https://www.cisco.com/site/us/en/learn/topics/security/what-is-an-incident-response-plan.html  
- IBM — What is incident response?: https://www.ibm.com/think/topics/incident-response  
