---
description: En el ejemplo siguiente se crea un temporizador que se señalizará después de un retraso de 10 segundos.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Usar objetos de temporizador de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668159"
---
# <a name="using-waitable-timer-objects"></a><span data-ttu-id="d35ad-103">Usar objetos de temporizador de espera</span><span class="sxs-lookup"><span data-stu-id="d35ad-103">Using Waitable Timer Objects</span></span>

<span data-ttu-id="d35ad-104">En el ejemplo siguiente se crea un temporizador que se señalizará después de un retraso de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="d35ad-104">The following example creates a timer that will be signaled after a 10 second delay.</span></span> <span data-ttu-id="d35ad-105">En primer lugar, el código usa la función [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) para crear un [objeto de temporizador](waitable-timer-objects.md)que se pueda esperar.</span><span class="sxs-lookup"><span data-stu-id="d35ad-105">First, the code uses the [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function to create a [waitable timer object](waitable-timer-objects.md).</span></span> <span data-ttu-id="d35ad-106">A continuación, usa la función [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para establecer el temporizador.</span><span class="sxs-lookup"><span data-stu-id="d35ad-106">Then it uses the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function to set the timer.</span></span> <span data-ttu-id="d35ad-107">El código usa la función [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para determinar cuándo se ha señalado el temporizador.</span><span class="sxs-lookup"><span data-stu-id="d35ad-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer has been signaled.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

int main()
{
    HANDLE hTimer = NULL;
    LARGE_INTEGER liDueTime;

    liDueTime.QuadPart = -100000000LL;

    // Create an unnamed waitable timer.
    hTimer = CreateWaitableTimer(NULL, TRUE, NULL);
    if (NULL == hTimer)
    {
        printf("CreateWaitableTimer failed (%d)\n", GetLastError());
        return 1;
    }

    printf("Waiting for 10 seconds...\n");

    // Set a timer to wait for 10 seconds.
    if (!SetWaitableTimer(hTimer, &liDueTime, 0, NULL, NULL, 0))
    {
        printf("SetWaitableTimer failed (%d)\n", GetLastError());
        return 2;
    }

    // Wait for the timer.

    if (WaitForSingleObject(hTimer, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());
    else printf("Timer was signaled.\n");

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d35ad-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d35ad-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d35ad-109">Usar temporizadores que esperan con una llamada a procedimiento asincrónica</span><span class="sxs-lookup"><span data-stu-id="d35ad-109">Using Waitable Timers with an Asynchronous Procedure Call</span></span>](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
