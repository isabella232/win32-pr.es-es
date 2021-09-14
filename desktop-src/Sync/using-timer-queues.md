---
description: En el ejemplo siguiente se crea una rutina de temporizador que ejecutará un subproceso desde una cola de temporizador después de un retraso de 10 segundos.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Uso de colas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d084a03eb25301f94361c1e7ca6b76dd9fee269
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068904"
---
# <a name="using-timer-queues"></a>Uso de colas de temporizador

En el ejemplo siguiente se crea una rutina de temporizador que ejecutará un subproceso desde una cola [de temporizador](timer-queues.md) después de un retraso de 10 segundos. En primer lugar, el código usa [**la función CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear un objeto de evento que se señala cuando se completa el subproceso timer-queue. A continuación, crea una cola de temporizador y un temporizador de la cola de temporizador, mediante las funciones [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) y [**CreateTimerQueueTimer,**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) respectivamente. El código usa la [**función WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para determinar cuándo se ha completado la rutina de temporizador. Por último, el código llama [**a DeleteTimerQueue**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) para limpiar.

Para obtener más información sobre la rutina de temporizador, [**vea WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
