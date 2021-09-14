---
description: En el ejemplo siguiente se muestra cómo se usa un controlador de terminación para asegurarse de que los recursos se liberan cuando finaliza la ejecución de un cuerpo de código guardado.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Usar un controlador de terminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164558"
---
# <a name="using-a-termination-handler"></a>Usar un controlador de terminación

En el ejemplo siguiente se muestra cómo se usa un controlador de terminación para asegurarse de que los recursos se liberan cuando finaliza la ejecución de un cuerpo de código guardado. En este caso, un subproceso usa la [**función EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para esperar la propiedad de un objeto de sección crítico. Cuando el subproceso termina de ejecutar el código protegido por la sección crítica, debe llamar a la función [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para que el objeto de sección crítica esté disponible para otros subprocesos. El uso de un controlador de terminación garantiza que esto ocurra. Para obtener más información, vea [objetos de sección críticos.](../sync/critical-section-objects.md)


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
