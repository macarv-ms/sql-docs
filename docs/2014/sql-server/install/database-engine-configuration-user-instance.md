---
title: "Database Engine Configuration - User Instance | Microsoft Docs"
ms.custom: ""
ms.date: "06/13/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "database-engine"
ms.tgt_pltfrm: ""
ms.topic: conceptual
f1_keywords: 
  - "database engine configuration"
  - "database engine configuration, user instance"
ms.assetid: dfc27c1e-0fe2-4221-bed5-f52667ddd3c8
caps.latest.revision: 11
author: "JennieHubbard"
ms.author: "jhubbard"
manager: craigg
---
# Database Engine Configuration - User Instance
  Use the **User Instance** page to generate a separate instance of the [!INCLUDE[ssDE](../../includes/ssde-md.md)] for users without administrator permissions, and to add users to the administrator role.  
  
## Option  
 Enable User Instances  
 Default is on. To disable the functionality of enabling user instances, clear the check box.  
  
 The user instance, also known as a child or client instance, is an instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] that is generated by the parent instance (the primary instance that runs as a service, like [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)]) on behalf of a user. The user instance runs as a user process under the security context of that user. The user instance is isolated from the parent instance and any other user instances running on the computer. The user instance feature is also referred to as “Run As Normal User” (RANU).  
  
> [!NOTE]  
>  Logins provisioned as members of the **sysadmin** fixed server role during setup are provisioned as administrators in the template database. They are members **sysadmin** fixed server role on the user instance unless removed  
  
 Add User to the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Administrator role  
 Default is not on. To add the current setup user to the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Administrator role, select the check box.  
  
 [!INCLUDE[wiprlhext](../../includes/wiprlhext-md.md)] users that are members of BUILTIN\Administrators are not automatically added to the sysadmin fixed server role when they connect to [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)]. Only [!INCLUDE[wiprlhext](../../includes/wiprlhext-md.md)] users that have been explicitly added to a server-level administrator role can administer [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)]. Any member of the Built-In\Users group can connect to the [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)] instance, but they will have limited permissions to perform database tasks. For this reason, users whose [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)] privileges are inherited from BUILTIN\Administrators and Built-In\Users in previous releases of Windows must be explicitly granted administrative privileges in instances of [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)] running on [!INCLUDE[wiprlhext](../../includes/wiprlhext-md.md)].  
  
 To make any changes to the user roles after this installation program ends, use the [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] Surface Area Configuration Tool (SQLSAC.exe). To update the list of users in the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] System Administrator role, click the **Add New Administrator** link.  
  
 Ensure that the **User to provision** field lists the DomainName\UserName of the user whose permissions should be updated. Select the role to be updated from the list of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] instances in the **Available privileges** pane, and then click the right arrow. To add the user to all available roles for all available instances of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] instances and all available roles, click the double right arrow.  
  
 To implement the changes when your selections are complete, [!INCLUDE[clickOK](../../includes/clickok-md.md)]. To end the tool without making changes, click **Cancel**.  
  
  