---
title: Probar si se está ejecutando en un controlador de dominio
description: En el código siguiente se usa la función VerifyVersionInfo para determinar si el proceso de llamada se está ejecutando en un controlador de dominio de servidor de Windows 2000.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149159"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="60d9f-103">Probar si se está ejecutando en un controlador de dominio</span><span class="sxs-lookup"><span data-stu-id="60d9f-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="60d9f-104">En el código siguiente se usa la función [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) para determinar si el proceso de llamada se está ejecutando en un controlador de dominio de servidor de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="60d9f-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="60d9f-105">El programa de instalación del servicio podría usar esta prueba antes de instalar un servicio con la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="60d9f-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="60d9f-106">Si la prueba indica que se está ejecutando en un controlador de dominio, instale el servicio para que se ejecute en una cuenta de usuario o muestre un cuadro de diálogo en el que se advierte de los peligros de ejecutar como LocalSystem en un controlador de dominio (que es que el servicio tendría acceso sin restricciones a Active Directory Domain Services, un contexto de seguridad muy eficaz que tiene la posibilidad de dañar toda la red).</span><span class="sxs-lookup"><span data-stu-id="60d9f-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 