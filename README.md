# DeployAzureAVD

## Overview
This project showcases the deployment and configuration of an Azure Virtual Desktop (AVD) environment integrated with an Active Directory domain controller. It involved setting up essential components to create a functional and secure virtual desktop infrastructure. The project demonstrates proficiency in various Azure services and configuration techniques.

## Purpose
The primary objective of this project was to:
* Deploy and configure an AVD environment.
* Integrate it with Active Directory for user and group management.
* Ensure proper setup of FSLogix and MSIX for profile and application management.
* Validate the deployment through thorough testing and demonstration.

## Project Diagram
![Project Diagram](avddiagram.png)


## Key Takeaways
1. Comprehensive Azure Virtual Desktop (AVD) Deployment
- Virtual Network (VNet) Setup:
  - Purpose: Establish a secure network environment for your VMs and services.
  - Implementation: Created a VNet with appropriate subnets and IP configurations to support the AVD infrastructure.
- Domain Controller Configuration:
  - Purpose: Manage user authentication and domain services.
  - Implementation: Deployed a Windows Server VM as a Domain Controller, configured Active Directory Domain Services, and created necessary domain users and groups.

2. Integration with Azure Active Directory (AAD)
- Global Administrator Setup:
  - Purpose: Ensure proper administrative access and integration with Azure services.
  - Implementation: Created and configured a Global Administrator account in Microsoft Entra ID to manage Azure AD settings.
- Azure AD Connect:
  - Purpose: Synchronize on-premises Active Directory with Azure AD.
  - Implementation: Installed Azure AD Connect on the Domain Controller VM to facilitate synchronization between AD DS and AAD.

3. User and Group Management
- Creation and Synchronization:
  - Purpose: Manage user access and permissions effectively.
  - Implementation: Created multiple users and groups in both AD DS and AAD, configured group memberships, and verified synchronization.
- Group Assignments:
  - Purpose: Control user access to resources.
  - Implementation: Assigned users to specific groups (e.g., Pool1_Users, RemoteApps) to manage access to application groups and resources.

4. Storage and File Share Configuration
- Azure Storage Account:
  - Purpose: Provide centralized storage for user profiles and data.
  - Implementation: Created a storage account and file share, configured AD DS authentication, and set up access controls for file shares.
- File Share Permissions:
  - Purpose: Ensure appropriate access levels for different user groups.
  - Implementation: Configured permissions for FS_Contributors and FS_Elevated_Contributors groups to manage access to the file share.

5. Multi-session VM Creation and Management
- VM Configuration:
  - Purpose: Provide users with a multi-session desktop experience.
  - Implementation: Deployed a Windows multi-session VM with Microsoft 365 Apps, installed FSLogix for profile management, and generalized the VM for scaling.
- Image Creation:
  - Purpose: Use a standardized VM image for deploying additional hosts.
  - Implementation: Created and managed a VM image to streamline the addition of new hosts to the host pool.

6. Host Pool and Application Groups
- Host Pool Setup:
  - Purpose: Manage and deploy virtual desktops efficiently.
  - Implementation: Configured a pooled host pool and associated it with the created VM image.
- Application Groups:
  - Purpose: Provide users with access to specific applications.
  - Implementation: Created application groups, added applications like Word, Excel, and PowerPoint, and assigned them to users.

7. Security and Testing
MFA Configuration:
  - Purpose: Enhance security by requiring multi-factor authentication for users.
  - Implementation: Configured MFA for all users and administrators to secure access.
- Testing and Validation:
  - Purpose: Ensure the AVD environment is functional and meets requirements.
  - Implementation: Conducted comprehensive testing, including logging in users, verifying MFA, checking application functionality, and validating profile updates.

## Demonstration
The project video has been recorded and uploaded to Microsoft Stream. The video demonstrates the setup, configuration, and validation of the AVD environment, including all required tasks. Here's the [link](https://drive.google.com/file/d/1zSAklFIwaa653S_ckipLIe9t7u-UtLTi/view?usp=sharing) to the video.

Thank you for reviewing my project. If you have any questions or feedback, please feel free to reach out.