**Project Overview**

This project demonstrates the implementation of a hybrid Identity and Access Management (IAM) environment using Active Directory Domain Services (AD DS) and Microsoft Entra ID.

The project involved creating an organizational group in Active Directory, configuring a shared folder for the Human Resources (HR) department, and implementing role-based file access permissions.

The HR manager was granted permission to modify files within the shared folder, while HR staff were restricted to read-only access. The on-premises Active Directory environment was then synchronized with Microsoft Entra ID to extend identity management to the cloud.

The project demonstrates how centralized identity management, group-based access control, and directory synchronization can support organizational security.

**Project Objectives**

Configure Active Directory Domain Services for centralized identity management.
Create an HR security group in Active Directory.
Configure a shared folder for HR departmental resources.
Apply different access permissions based on job responsibilities.
Grant the HR manager permission to modify files.
Restrict HR staff to read-only access.
Synchronize on-premises identities with Microsoft Entra ID.
Validate permissions and document the results.

**Tools and Technologies**
    1. Windows Server
    2. Active Directory Domain Services (AD DS)
    3. Active Directory Users and Computers
    4. Windows file sharing
    5. NTFS file system permissions
    6. Microsoft Entra ID
    7. Microsoft Entra Connect Sync, if used for synchronization
    8. Windows File Explorer and file access testing

**Implementation**

1. Active Directory Configuration

I Created an organizational group in Active Directory Domain Services to manage access to HR resources.

The group provides a centralized way to organize users and assign access according to their responsibilities.

<img width="1920" height="1012" alt="groups" src="https://github.com/user-attachments/assets/43bcdf51-5785-46db-98c6-23fec33342b5" />
<img width="1920" height="1012" alt="manager group memebr" src="https://github.com/user-attachments/assets/3a08604a-b192-4dc8-965f-96ee434aea51" />
<img width="1920" height="1012" alt="hr group memebr" src="https://github.com/user-attachments/assets/e9ced0f4-5ef5-4a1b-b5cf-2da0af4550d1" />

2. HR Shared Folder Creation

Created a shared folder dedicated to the Human Resources department.

<img width="1920" height="1012" alt="hr shared folder" src="https://github.com/user-attachments/assets/a63cf345-721b-444e-8dee-18f0624cea2a" />


The folder provides a central location for storing and accessing HR documents within the organization's local network.

3. Role-Based Access Control.

I Configured permissions according to the responsibilities of the HR manager and HR staff.
User/Role	Access level	Allowed activities
HR Manager	Read and Modify	View, create, edit, and delete files, subject to the configured permissions
HR Staff	Read-only	View and open permitted files
Unauthorized users	No access	Access denied

<img width="1920" height="1012" alt="VirtualBox_win-svr_22_10_2026_07_30_40" src="https://github.com/user-attachments/assets/a7232392-1882-4dfd-99c9-1e3470af67c6" />
<img width="1920" height="1012" alt="VirtualBox_win-svr_22_10_2026_07_30_49" src="https://github.com/user-attachments/assets/4ea97c6c-3033-4d3f-a2a4-a5954e6b20ff" />


Access was assigned according to job responsibilities to reduce unnecessary permissions and support the principle of least privilege.
4. Permission Configuration

Configured access permissions for the HR shared folder.

The effective permissions depend on both the SMB share permissions and NTFS permissions. Where both apply, the effective access is constrained by the combination of those permissions.

The manager's permissions were configured to allow modification, while HR staff were restricted to read-only access.
5. Microsoft Entra ID Synchronization

**Testing and Validation**
<img width="1920" height="1012" alt="manager test" src="https://github.com/user-attachments/assets/d3c96cb6-1f06-46ed-b49d-cf7b88f71dc0" />
<img width="1920" height="1012" alt="hr user permission testing" src="https://github.com/user-attachments/assets/feba3617-3cb0-4389-9870-6856aa0b8cef" />

**Microsoft Entra syn Environment**

<img width="953" height="422" alt="Screenshot 2026-10-22 064048" src="https://github.com/user-attachments/assets/e84fbcf8-f13e-45b6-956c-321da2e52349" />
<img width="948" height="434" alt="Screenshot 2026-10-22 063811" src="https://github.com/user-attachments/assets/a703c139-52a7-457c-bb29-7d5c3c699f35" />
<img width="949" height="311" alt="Screenshot 2026-10-22 063919" src="https://github.com/user-attachments/assets/df468a33-e8dc-4c39-9d1e-323eb505d839" />
<img width="955" height="416" alt="Screenshot 2026-10-22 064019" src="https://github.com/user-attachments/assets/1e32fd68-6a8c-4bf4-b428-bc6ba4021186" />
