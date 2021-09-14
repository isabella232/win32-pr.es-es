---
description: En el ejemplo siguiente se crea un temporizador que se señalizará después de un retraso de 10 segundos.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Usar objetos de temporizador que se pueden esperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068898"
---
# <a name="using-waitable-timer-objects"></a>Usar objetos de temporizador que se pueden esperar

En el ejemplo siguiente se crea un temporizador que se señalizará después de un retraso de 10 segundos. En primer lugar, el código usa [**la función CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) para crear un objeto [de temporizador que se puede esperar.](waitable-timer-objects.md) A continuación, usa [**la función SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para establecer el temporizador. El código usa la [**función WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para determinar cuándo se ha señalado el temporizador.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar temporizadores que se pueden esperar con una llamada a procedimiento asincrónico](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
