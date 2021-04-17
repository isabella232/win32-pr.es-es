---
description: En el ejemplo siguiente se usa la función ExitWindowsEx para apagar el sistema.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Cómo apagar el sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667181"
---
# <a name="how-to-shut-down-the-system"></a>Cómo apagar el sistema

En el ejemplo siguiente se usa la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para apagar el sistema. Al cerrarse, se vacían los búferes de archivos en el disco y se pone al sistema en una condición en la que es seguro apagar el equipo. En primer lugar, la aplicación debe habilitar el privilegio de nombre de cierre de SE \_ \_ . Para obtener más información, vea [privilegios](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



El último parámetro de la llamada a [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indica que el sistema se apagó para una actualización de planeación del sistema operativo. Para obtener más información, consulte [códigos de motivo de apagado del sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apagar](shutting-down.md)
</dt> </dl>

 

 
