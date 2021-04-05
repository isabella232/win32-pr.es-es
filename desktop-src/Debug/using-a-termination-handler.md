---
description: En el ejemplo siguiente se muestra cómo se utiliza un controlador de terminación para asegurarse de que los recursos se liberan cuando finaliza la ejecución de un cuerpo protegido de código.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Usar un controlador de terminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000587"
---
# <a name="using-a-termination-handler"></a><span data-ttu-id="d4169-103">Usar un controlador de terminación</span><span class="sxs-lookup"><span data-stu-id="d4169-103">Using a Termination Handler</span></span>

<span data-ttu-id="d4169-104">En el ejemplo siguiente se muestra cómo se utiliza un controlador de terminación para asegurarse de que los recursos se liberan cuando finaliza la ejecución de un cuerpo protegido de código.</span><span class="sxs-lookup"><span data-stu-id="d4169-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="d4169-105">En este caso, un subproceso utiliza la función [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para esperar la propiedad de un objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="d4169-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="d4169-106">Cuando el subproceso termina de ejecutar el código que está protegido por la sección crítica, debe llamar a la función [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para que el objeto de sección crítica esté disponible para otros subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d4169-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="d4169-107">El uso de un controlador de terminación garantiza que esto ocurrirá.</span><span class="sxs-lookup"><span data-stu-id="d4169-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="d4169-108">Para obtener más información, vea [objetos de sección crítica](../sync/critical-section-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d4169-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


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



 

 
