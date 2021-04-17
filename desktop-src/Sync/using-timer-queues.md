---
description: En el ejemplo siguiente se crea una rutina de temporizador que se ejecutará en un subproceso desde una cola de temporizador después de un retraso de 10 segundos.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Usar colas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13f7afd18a22c42e3af8cffd8b2b148f68b9d99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668160"
---
# <a name="using-timer-queues"></a><span data-ttu-id="c41b2-103">Usar colas de temporizador</span><span class="sxs-lookup"><span data-stu-id="c41b2-103">Using Timer Queues</span></span>

<span data-ttu-id="c41b2-104">En el ejemplo siguiente se crea una rutina de temporizador que se ejecutará en un subproceso desde una [cola de temporizador](timer-queues.md) después de un retraso de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="c41b2-104">The following example creates a timer routine that will be executed by a thread from a [timer queue](timer-queues.md) after a 10 second delay.</span></span> <span data-ttu-id="c41b2-105">En primer lugar, el código usa la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear un objeto de evento que se señala cuando se completa el subproceso de cola de temporizador.</span><span class="sxs-lookup"><span data-stu-id="c41b2-105">First, the code uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create an event object that is signaled when the timer-queue thread completes.</span></span> <span data-ttu-id="c41b2-106">A continuación, crea una cola de temporizador y un temporizador de cola de temporizador, mediante las funciones [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) y [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c41b2-106">Then it creates a timer queue and a timer-queue timer, using the [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) and [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) functions, respectively.</span></span> <span data-ttu-id="c41b2-107">El código usa la función [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para determinar cuándo se ha completado la rutina del temporizador.</span><span class="sxs-lookup"><span data-stu-id="c41b2-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer routine has completed.</span></span> <span data-ttu-id="c41b2-108">Por último, el código llama a [**DeleteTimerQueue**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue) para realizar la limpieza.</span><span class="sxs-lookup"><span data-stu-id="c41b2-108">Finally, the code calls [**DeleteTimerQueue**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue) to clean up.</span></span>

<span data-ttu-id="c41b2-109">Para obtener más información sobre la rutina del temporizador, vea [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c41b2-109">For more information on the timer routine, see [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span></span>


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



 

 
