# Microsoft-SC-900

## Concepts of Security, Compliance and Identity
Zero Trust Methodology: There are three principles which define this; Verify Explicitly, Use less Privilege Access and assume breach, which means firewall is not always safe.
Use every method to validate identity and authorization: Just In Time (JIT), Just Enough Access (JEA).

Identity: Verify and secure each identity.
Devices: Ensure compliance (TLS)
Application: Monitor user actions and in application permissions
Data: Encrypt to protect data and restrict access
Infra: Monitor to detect attacks, block and flag risky behavior
Network: Encrypt all communication

## Defense in Depth
Common Threats include Data threats which occur due to Phishing, Scams, SQL Injection or Trojan Malware.
Dictionary Attack means the attacker is attempting brute force attacks.
Ransomware is demanding ransomware for decrypting.

## Encryption
Hashing: Creates digital signature but is not technically encryption.
Hash collision means hashes are not unique

---

Identity is primary security perimeter. Monitor to detect strange behavior and restrict unrequired/unwanted network traffic.
Authorization: It is the level of access authenticated to a person AKA permissions which the person holds.
Authentication: This is to prove the identity of the person.
Identity provider creates, maintains, manages ID information also offers authentication and authorization.
Domain Controller is server which hosts Active Directory. This maintains and manages permission on that network. Active Directory (basic) does not work over the internet.
Azure AD Conditional Access: Uses signals to make decisions and enforce policies, where signals can be users, device location.
Claims Based Access Control (CBAC): Access control paradigm that users claim to make access control decisions to resources.
ID Governance: Balance between security and productivity.

## Azure Network Security Groups/Access Control Lists
The simple rule based control that allows or denies traffic travelling over network boundary.
There are separate rules for inbound and out band traffic.
The 2 network boundaries that NSG apply is at subnet level, other is at VM or NIC level.
‘Deny at Default Policy’ any traffic from internet into network is denied unless explicitly permitted.
Azure Firewall: has different levels of network stack at the application level or at network level. It has automatic threat intelligence.
Azure Bastion: allows administrators to get access to Azure VMs with exposing to public internet. Bastion AKA Jump Box.
Azure WAF: Can be added to application gateway.
Application gateway is type of load balancer. Based on common rules set by OWASP, can create custom rules and also geographic rules.

## Azure Key Vault
These are customer managed keys stored in Key Vault. And key vault is designed to store secrets, certificates.
This requires Authentication and Authorization to access keys which means no storing as a file in disk.
This can remove key from storage, code, source control and can generate new keys.

## Azure Security Center (Infra Security Management)
Cloud Security Posture Management — assessments and recommendations.
Cloud Workload Protection (firewalls).
Supports PaaS like Application Service plans.
Azure Defender — Cloud Workload Protector.
Azure Sentinel [SIEM/SOAR]—Collecting data and ‘Workbooks’ create report as Sentinel is used to detect threats in organization.

## Microsoft 365 Defender
This is a united suite of enterprise defense and integrated service.
MS 365 for Identity — Formerly called as Advanced Threat Protection (ATP) which is an Azure Directory Connected service.
This uses Azure AD data, signals to protect identities. And also can identify behavior anomalies, security reports, user profile analytics.
Designed to reduce general alert, provide only relevant information and important security alerts in real time attack timeline.
MS 365 for Office — Checks for malicious activities in Office apps.
MS 365 for Endpoint — AKA ‘devices’ (laptops, phones)
MS 365 for Security Centre — This manages security across identities, data, devices, applications and infra. It also makes recommendation for improvements, which is similar to Azure Security Score.

Compliance Portal — This helps to understand, manage an organization’s compliance needs.
Retention Policies — Is applied at site or mailbox level and to multiple location. These inherit retention from containers.
Data Loss Prevention — These protect sensitive information and prevent data disclosure.
Azure Resource Locks — Apply lock at parent scope and all the resources present will inherit lock.
---
