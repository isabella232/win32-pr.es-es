---
title: Probar si se ejecuta en un controlador de dominio
description: El código siguiente usa la función VerifyVersionInfo para determinar si el proceso de llamada se ejecuta en un controlador de dominio Windows Server 2000.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024593"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Probar si se ejecuta en un controlador de dominio

El código siguiente usa la [**función VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) para determinar si el proceso de llamada se ejecuta en un controlador de dominio Windows Server 2000. El programa de instalación del servicio podría usar esta prueba antes de instalar un servicio en la cuenta LocalSystem. Si la prueba indica que se está ejecutando en un controlador de dominio, instale el servicio para que se ejecute con una cuenta de usuario o muestre una advertencia de cuadro de diálogo de los riesgos de ejecutarse como LocalSystem en un controlador de dominio (que es que el servicio tendría acceso sin restricciones a Active Directory Domain Services, un contexto de seguridad muy eficaz que tiene el potencial de dañar toda la red).


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



 

 