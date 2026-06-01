# Enterprise Active Directory & RBAC Lab

## Overview

This lab demonstrates the deployment and administration of an Enterprise Active Directory environment using Windows Server 2022 and Windows 11.

The objective was to implement a secure domain environment with Organizational Units (OUs), users, security groups, Role-Based Access Control (RBAC) and department file share permissions.

---

## Environment

| Component | Description |
|------------|------------|
| Domain Controller | Windows Server 2022 |
| Client Workstation | Windows 11 Pro |
| Domain Name | corp.local |
| Departments | HR, Finance, IT |
| Security Groups | HR_Users, Finance_Users, IT_Admins |

---

## Architecture

```text
DC01 (Windows Server 2022)
│
├── HR OU
│   └── JohnHR
│
├── Finance OU
│   └── DavidFinance
│
├── IT OU
│   └── AsadAdmin
│
└── Workstations OU
    └── Client01
```

---

## Lab Objectives

- Deploy Active Directory Domain Services
- Configure a Domain Controller
- Create Organizational Units
- Create departmental users
- Create security groups
- Implement Role-Based Access Control
- Join Windows 11 workstation to domain
- Configure secure file shares
- Validate least-privilege access

---

## Organizational Units

- HR
- Finance
- IT
- Workstations

---

## Users Created

### HR Department

- JohnHR

### Finance Department

- DavidFinance

### IT Department

- AsadAdmin

---

## Security Groups

- HR_Users
- Finance_Users
- IT_Admins

---

## File Share Permissions

### HR Share

Allowed:
- HR_Users

Denied:
- Finance_Users

### Finance Share

Allowed:
- Finance_Users

Denied:
- HR_Users

---

## Access Validation

| User | HR Share | Finance Share |
|--------|---------|---------------|
| JohnHR | ✅ Allowed | ❌ Denied |
| DavidFinance | ❌ Denied | ✅ Allowed |

---

## Key IAM Concepts Demonstrated

- Identity Lifecycle Management
- Role-Based Access Control (RBAC)
- Group-Based Authorization
- Organizational Unit Management
- Access Governance
- Least Privilege Access
- Authentication and Authorization
- Access Validation Testing

---

## Skills Demonstrated

- Active Directory Administration
- Identity & Access Management
- RBAC
- Organizational Unit Management
- Windows Server 2022
- Domain Services
- Windows Security
- NTFS Permissions
- Access Control
- Least Privilege

---

## Evidence

All screenshots documenting deployment, configuration, RBAC implementation, permission assignments and access validation testing are available in the Screenshots folder.

---

## Author

Asad

SC-300 | Security+ | Identity & Access Management | Cybersecurity
