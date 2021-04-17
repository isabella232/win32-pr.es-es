---
description: En el ejemplo siguiente se reinicia el sistema local mediante la función InitiateSystemShutdown.
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: Mostrar el cuadro de diálogo de apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667182"
---
# <a name="displaying-the-shutdown-dialog-box"></a><span data-ttu-id="9371e-103">Mostrar el cuadro de diálogo de apagado</span><span class="sxs-lookup"><span data-stu-id="9371e-103">Displaying the Shutdown Dialog Box</span></span>

<span data-ttu-id="9371e-104">En el ejemplo siguiente se reinicia el sistema local mediante la función [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) .</span><span class="sxs-lookup"><span data-stu-id="9371e-104">The following example reboots the local system using the [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) function.</span></span> <span data-ttu-id="9371e-105">El sistema muestra un cuadro de diálogo con un mensaje personalizado y un mensaje al usuario para cerrar las aplicaciones en el intervalo de tiempo de espera especificado (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="9371e-105">The system displays a dialog box with a custom message and a message to the user to close applications within the specified time-out interval (30 seconds).</span></span> <span data-ttu-id="9371e-106">Una vez transcurrido el intervalo de tiempo de espera, se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="9371e-106">After the time-out interval elapses, the system is restarted.</span></span>

<span data-ttu-id="9371e-107">La aplicación debe habilitar el privilegio de nombre de cierre de SE \_ antes de \_ llamar a [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna).</span><span class="sxs-lookup"><span data-stu-id="9371e-107">The application must enable the SE\_SHUTDOWN\_NAME privilege before calling [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna).</span></span> <span data-ttu-id="9371e-108">Para obtener más información, vea [privilegios](../secauthz/privileges.md).</span><span class="sxs-lookup"><span data-stu-id="9371e-108">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



<span data-ttu-id="9371e-109">Si la función [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) se ejecuta en el período de tiempo de espera especificado por [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), el sistema no se apaga.</span><span class="sxs-lookup"><span data-stu-id="9371e-109">If the [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) function is executed in the time-out period specified by [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), the system does not shut down.</span></span> <span data-ttu-id="9371e-110">Por ejemplo, si se llama a PreventSystemShutdown después de MySystemShutdown, el sistema cierra el cuadro de diálogo y no reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="9371e-110">For example, if PreventSystemShutdown is called after MySystemShutdown, the system closes the dialog box and does not restart the system.</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
