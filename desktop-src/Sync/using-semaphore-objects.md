---
description: En el ejemplo siguiente se usa un objeto semáforo para limitar el número de subprocesos que pueden realizar una tarea determinada.
ms.assetid: 24a5c13c-573a-4fc2-ac19-98188c9eb68a
title: Usar objetos semáforos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66ca0dc941852efd20d1d17bca1c1730fb6bac9782c86c50ef8fdd9e94bd043
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034695"
---
# <a name="using-semaphore-objects"></a>Usar objetos semáforos

En el ejemplo siguiente se usa [un objeto semáforo](semaphore-objects.md) para limitar el número de subprocesos que pueden realizar una tarea determinada. En primer lugar, usa la función [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) para crear el semáforo y para especificar los recuentos iniciales y máximos, y luego usa la [**función CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para crear los subprocesos.

Antes de que un subproceso intente realizar la tarea, usa la función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) para determinar si el recuento actual del semáforo permite hacerlo. El parámetro de tiempo de espera de la función wait se establece en cero, por lo que la función devuelve inmediatamente si el semáforo está en estado no con signo. **WaitForSingleObject** disminuye el recuento del semáforo en uno.

Cuando un subproceso completa la tarea, usa la función [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para incrementar el recuento del semáforo, lo que permite que otro subproceso en espera realice la tarea.


```C++
#include <windows.h>
#include <stdio.h>

#define MAX_SEM_COUNT 10
#define THREADCOUNT 12

HANDLE ghSemaphore;

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a semaphore with initial and max counts of MAX_SEM_COUNT

    ghSemaphore = CreateSemaphore( 
        NULL,           // default security attributes
        MAX_SEM_COUNT,  // initial count
        MAX_SEM_COUNT,  // maximum count
        NULL);          // unnamed semaphore

    if (ghSemaphore == NULL) 
    {
        printf("CreateSemaphore error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) ThreadProc, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and semaphore handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghSemaphore);

    return 0;
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult; 
    BOOL bContinue=TRUE;

    while(bContinue)
    {
        // Try to enter the semaphore gate.

        dwWaitResult = WaitForSingleObject( 
            ghSemaphore,   // handle to semaphore
            0L);           // zero-second time-out interval

        switch (dwWaitResult) 
        { 
            // The semaphore object was signaled.
            case WAIT_OBJECT_0: 
                // TODO: Perform task
                printf("Thread %d: wait succeeded\n", GetCurrentThreadId());
                bContinue=FALSE;            

                // Simulate thread spending time on task
                Sleep(5);

                // Release the semaphore when task is finished

                if (!ReleaseSemaphore( 
                        ghSemaphore,  // handle to semaphore
                        1,            // increase count by one
                        NULL) )       // not interested in previous count
                {
                    printf("ReleaseSemaphore error: %d\n", GetLastError());
                }
                break; 

            // The semaphore was nonsignaled, so a time-out occurred.
            case WAIT_TIMEOUT: 
                printf("Thread %d: wait timed out\n", GetCurrentThreadId());
                break; 
        }
    }
    return TRUE;
}
```



 

 
