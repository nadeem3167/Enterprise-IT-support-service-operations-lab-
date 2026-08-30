# Enterprise-IT-support-service-operations-lab-
Hands-on Windows enterprise IT support lab covering Active Directory, DNS, DHCP, Group Policy, access control, troubleshooting and ServiceNow incident management.
# Enterprise IT Support & Service Operations Lab

## Overview

This project is a hands-on enterprise IT support lab built to develop practical experience with Windows administration, Active Directory, networking, access control, Group Policy, troubleshooting, and IT service management.

The environment simulates a small corporate network where users, workstations, servers, permissions, policies, and support incidents are managed using common enterprise technologies.

## Lab Environment

- Windows Server 2022
- Windows 11 Pro
- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- Windows File Services
- ServiceNow
- Oracle VirtualBox

### Architecture

The environment consists of:

- **DC01** — Domain Controller and DNS server
- **SRV01** — DHCP and File Server
- **CLIENT01** — Domain-joined Windows 11 workstation
- **Domain:** `corp.lab`
- **Network:** `10.10.10.0/24`

## Active Directory Administration

Configured an Active Directory environment containing departmental organisational units for:

- IT
- Finance
- HR
- Sales

Created and managed domain users, security groups, computers, service accounts, and disabled-user containers.

Implemented role-based access using the **AGDLP model**:

`User Accounts → Global Groups → Domain Local Groups → Permissions`

This allowed departmental access to be managed through group membership rather than assigning permissions directly to individual users.

## File Services and Access Control

Configured departmental file sharing on SRV01.

Implemented:

- SMB file shares
- Share permissions
- NTFS permissions
- Security-group-based access
- Least-privilege access controls

Tested both authorised and unauthorised access to confirm that permissions were functioning correctly.

## Group Policy

Created and applied Group Policies for domain workstations and users.

Examples included:

- Departmental mapped network drives
- Windows Firewall enforcement
- Automatic workstation locking after inactivity
- Centralised workstation security configuration

Used tools such as:

`gpupdate`

`gpresult`

to refresh and verify Group Policy application.

## DNS and DHCP

Configured DNS to support Active Directory and internal name resolution.

Configured DHCP on SRV01 including:

- Address scopes
- IP address allocation
- Subnet configuration
- Default gateway
- DNS server configuration
- Domain information

Practised diagnosing network issues involving DHCP leases, missing gateway configuration, DNS resolution, and client connectivity.

## User Lifecycle Management

Performed common IT administration tasks including:

- Creating new users
- Assigning users to departments
- Managing security-group membership
- Providing access to departmental resources
- Disabling leaver accounts
- Removing access during offboarding

## IT Support and Troubleshooting

Practised structured troubleshooting across several common support scenarios, including:

- User authentication and account lockout
- Shared-folder access problems
- Group membership and permissions issues
- DHCP and default-gateway problems
- Group Policy issues
- Network connectivity
- DNS and infrastructure-related incidents

Common troubleshooting tools included:

- `ipconfig`
- `ping`
- `nslookup`
- `gpupdate`
- `gpresult`
- `whoami`
- `nltest`
- Windows administrative consoles

## ServiceNow / ITSM

Used a ServiceNow Personal Developer Instance to practise IT service-management workflows.

Created and managed incidents involving:

- User authentication
- File-access problems
- Network connectivity
- Group Policy
- Infrastructure outages

Practised an incident lifecycle of:

`Issue Reported → Investigation → Work Notes → Diagnosis → Resolution → Verification → Closure`

Worked with concepts including:

- Impact
- Urgency
- Priority
- Incident states
- Work notes
- Resolution codes
- Resolution documentation

## Key Troubleshooting Example

One workstation successfully received an IP address and DNS configuration from DHCP but could not access external networks.

Investigation showed that the DHCP lease did not contain a default gateway.

The issue was traced to the DHCP scope configuration on SRV01. After restoring the router/default-gateway option and renewing the client's DHCP lease, connectivity was successfully restored.

This demonstrated the importance of troubleshooting network connectivity layer-by-layer rather than assuming that receiving an IP address means the network configuration is complete.

## Skills Demonstrated

- Windows Server Administration
- Active Directory
- DNS
- DHCP
- Group Policy
- Windows 11 Administration
- TCP/IP Networking
- User and Group Management
- AGDLP
- NTFS Permissions
- SMB File Sharing
- Role-Based Access Control
- IT Troubleshooting
- ServiceNow
- Incident Management
- ITSM Fundamentals
- Technical Documentation

## Project Outcome

This project provided practical experience operating a small Windows enterprise environment rather than only studying the technologies theoretically.

The main focus was understanding how identity, networking, permissions, policies, infrastructure services, and IT support processes interact when supporting users in a business environment.
