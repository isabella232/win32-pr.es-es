---
description: Las aplicaciones pueden usar objetos de evento en varias situaciones para notificar a un subproceso en espera la aparición de un evento.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Usar objetos de evento (sincronización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50fdca3994aa5ecb6ea2b0a2dde4ba5a2527c7d6
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521362"
---
# <a name="using-event-objects-synchronization"></a>Usar objetos de evento (sincronización)

Las aplicaciones pueden usar [objetos de evento](event-objects.md) en varias situaciones para notificar a un subproceso en espera la aparición de un evento. Por ejemplo, las operaciones de E/S superpuestas en archivos, canalizaciones con nombre y dispositivos de comunicaciones usan un objeto de evento para indicar su finalización. Para obtener más información sobre el uso de objetos de evento en operaciones de E/S superpuestas, vea [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).

En el ejemplo siguiente se usan objetos de evento para evitar que varios subprocesos lean desde un búfer de memoria compartido mientras un subproceso maestro escribe en ese búfer. En primer lugar, el subproceso maestro usa la [**función CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear un objeto de evento de restablecimiento manual cuyo estado inicial no essignaled. A continuación, crea varios subprocesos de lector. El subproceso maestro realiza una operación de escritura y, a continuación, establece el objeto de evento en el estado señalado cuando ha terminado de escribir.

Antes de iniciar una operación de lectura, cada subproceso de lector usa [**WaitForSingleObject para**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) esperar a que se señale el objeto de evento de restablecimiento manual. Cuando **se devuelve WaitForSingleObject,** esto indica que el subproceso principal está listo para que comience su operación de lectura.


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
