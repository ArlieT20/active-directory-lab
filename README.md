# active-directory-lab
# Active Directory Domain Controller Lab

## Overview

This project demonstrates the deployment of a Windows Server 2022 Domain Controller using Active Directory Domain Services (AD DS) in a virtualized environment. The lab simulates a real-world enterprise network where centralized authentication, user management, and security policies are enforced.

---

## Objectives

* Deploy a domain controller
* Configure centralized authentication
* Manage users and password policies
* Simulate real-world IT support tasks

---

## Architecture

* Domain Controller: Windows Server 2022 (DC01)
* Client Machine: Windows 11 (CLIENT1)
* Network: NAT (VMware)
* Domain: corp.local

---

## Technologies Used

* VMware Workstation Pro
* Windows Server 2022
* Windows 11
* Active Directory Domain Services (AD DS)
* Group Policy Management

---

## Implementation

### 1. Server Setup

* Installed Windows Server 2022
* Renamed server to DC01
* Configured static IP (192.168.1.10)
* Set DNS to localhost (127.0.0.1)

### 2. Active Directory Configuration

* Installed AD DS role
* Promoted server to Domain Controller
* Created domain: corp.local

### 3. User Management

* Created Organizational Unit (Employees)
* Added users: john.doe, jane.smith
* Configured password reset and forced password changes

### 4. Group Policy (Security)

* Configured account lockout policy:

  * Threshold: 5 attempts
  * Duration: 15 minutes
* Enforced password policies

### 5. Client Integration

* Installed Windows 11
* Joined machine to domain (corp.local)
* Logged in using domain credentials
* Verified authentication workflow

---

## Testing & Validation

* Successfully logged in as domain users
* Forced password changes on first login
* Simulated failed login attempts → account lockout triggered
* Reset and unlocked accounts from Domain Controller

---

## Challenges & Solutions

* EFI Network Timeout → fixed by adjusting boot settings
* Windows installation error → resolved by removing virtual floppy device in VMware
* Domain join issues → corrected DNS configuration

---

## Key Takeaways

* Understanding of centralized authentication systems
* Experience managing users in Active Directory
* Hands-on implementation of security policies using Group Policy
* Real-world troubleshooting of system and network issues

---

## Screenshots

* Active Directory Users and Computers
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/284cb419-ede4-4279-a6c3-006d5fcc2e48" />
* Group Policy settings
<img width="1919" height="1040" alt="image" src="https://github.com/user-attachments/assets/b21d7605-a85b-41df-b407-9bb2b772bcdf" />
* Domain login screen
<img width="1918" height="963" alt="image" src="https://github.com/user-attachments/assets/8bbde401-34b6-4bb1-989b-49b1b31c7cdc" />

