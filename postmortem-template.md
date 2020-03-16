## `<Summary>` - POSTMORTEM - `<DATE>`
Incident number (if applicable): `<inc number>`

Authors: `<names>`

Status: __active__/__resolved__/__WIP__

Summary: *x* service was down for *dt* minutes for *y, z* reasons.

Impact:
* Application/service impact
* Impact to company revenue, if applicable

Root causes:
"*x* was down due to *a, b, c* reasons..." This is a technical discussion on WHAT happened after the trigger event and __Not the trigger__ itself. This should contain no waffle __no waffle__ and should be to the point and concise  eg: "Service *x* stopped accepting connection as the broker db had been cleared, meaning all credentials were missing. It was discovered late as the changes to the database were not discovered until restart."

Triggers:
Discuss the reasons behind the error occurring, __without naming names__. It is key to try and keep a blameless culture within the team. eg. "An upgrade to service *x* had been pushed through to production, and nobody realised during the PR that the read/write database user was missing from the release."

Resolution:
Discuss how the incident was resolved. Don't use pronouns such as I/he/she. eg. "The correct read/write permissions were giving to the database user, then the service was redeployed."

Detection:
Did your monitoring detect this incident? If so, what monitoring? Was it a person calling us? If so, who detected it and what team were they from?

## Action Items: 
Action Item | Type | Owner | Status
------------ | ------------- | --------------- | ---------------
Update testing to stop continuous deployment on upgrades | mitigate/prevent/process/other | `<name>` | TODO/DONE
Freeze Prod for *x* weeks to balance error budget | other | <team-name> | DONE

What went well:

* item 1
* item 2

What went badly:
* item 1
* item 2

Where we got lucky:
* item 1
* item 2

## Timeline:
`<DATE>`
  * `<TIME>` - Oldest item
  * `<TIME>` - Newest item

## Supporting Information
* anything like dashboards of outage

