\# When NOT to Isolate an Endpoint



This playbook defines scenarios where \*\*endpoint isolation is inappropriate\*\*

or \*\*high-risk\*\*, even when security alerts are present.



The goal is to prevent \*\*security response actions from causing more harm

than the incident itself\*\*.



---



\## Why this playbook exists



Isolation is often viewed as a default containment action.

In reality, it is a \*\*high-impact decision\*\* that can:



\- Disrupt business operations

\- Break authentication flows

\- Interrupt investigations

\- Cause secondary outages



Good incident response requires knowing \*\*when to stop\*\*.



---



\## Scenario 1: Critical Infrastructure Systems



Do \*\*not\*\* isolate endpoints that are:



\- Domain controllers

\- Identity federation services

\- Certificate authorities

\- Jump hosts or bastion systems

\- Production servers with no redundancy



\*\*Rationale:\*\*  

Isolation may cause widespread authentication failures or service outages.



---



\## Scenario 2: Unverified or Low-Confidence Alerts



Do \*\*not\*\* isolate when:



\- Alerts are informational or low severity

\- Detections are noisy or newly deployed

\- The alert lacks corroborating signals



\*\*Rationale:\*\*  

False positives combined with isolation create unnecessary outages.



---



\## Scenario 3: Active Investigations



Do \*\*not\*\* isolate when:



\- The endpoint is being used to observe attacker behavior

\- Isolation would tip off an adversary prematurely

\- Additional telemetry is still being collected



\*\*Rationale:\*\*  

Isolation can destroy valuable investigative context.



---



\## Scenario 4: Shared or Multi-User Systems



Do \*\*not\*\* isolate when:



\- Multiple users share the endpoint

\- Isolation would impact unrelated users

\- The blast radius is unclear



\*\*Rationale:\*\*  

Containment should be precise, not disruptive.



---



\## Scenario 5: Business-Critical Timing



Do \*\*not\*\* isolate during:



\- Critical business operations

\- Regulatory reporting windows

\- Known maintenance activities



\*\*Rationale:\*\*  

Timing matters as much as technical risk.



---



\## Required actions instead of isolation



When isolation is deferred:

\- Increase monitoring

\- Apply non-enforcing tags

\- Notify stakeholders

\- Escalate for human review



Containment is one tool — not the only one.



---



\## Summary



Effective incident response is not about acting fast.

It is about acting \*\*deliberately\*\*.



Knowing when \*\*not\*\* to isolate

is a hallmark of mature security operations.



