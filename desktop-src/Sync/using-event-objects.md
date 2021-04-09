---
description: Las aplicaciones pueden usar objetos de eventos en una serie de situaciones para notificar a un subproceso en espera de la aparición de un evento.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Usar objetos de eventos (sincronización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c0c7ee5f58b8359e989b19ffc9c016dd1a6593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910021"
---
# <a name="using-event-objects-synchronization"></a><span data-ttu-id="26ea4-103">Usar objetos de eventos (sincronización)</span><span class="sxs-lookup"><span data-stu-id="26ea4-103">Using Event Objects (Synchronization)</span></span>

<span data-ttu-id="26ea4-104">Las aplicaciones pueden usar [objetos de eventos](event-objects.md) en una serie de situaciones para notificar a un subproceso en espera de la aparición de un evento.</span><span class="sxs-lookup"><span data-stu-id="26ea4-104">Applications can use [event objects](event-objects.md) in a number of situations to notify a waiting thread of the occurrence of an event.</span></span> <span data-ttu-id="26ea4-105">Por ejemplo, las operaciones de e/s superpuestas en archivos, canalizaciones con nombre y dispositivos de comunicaciones usan un objeto de evento para indicar su finalización.</span><span class="sxs-lookup"><span data-stu-id="26ea4-105">For example, overlapped I/O operations on files, named pipes, and communications devices use an event object to signal their completion.</span></span> <span data-ttu-id="26ea4-106">Para obtener más información sobre el uso de objetos de eventos en operaciones de e/s superpuestas, vea [sincronización y entrada y salida superpuestas](synchronization-and-overlapped-input-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="26ea4-106">For more information about the use of event objects in overlapped I/O operations, see [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).</span></span>

<span data-ttu-id="26ea4-107">En el ejemplo siguiente se usan objetos de evento para evitar que varios subprocesos lean desde un búfer de memoria compartida mientras un subproceso maestro está escribiendo en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="26ea4-107">The following example uses event objects to prevent several threads from reading from a shared memory buffer while a master thread is writing to that buffer.</span></span> <span data-ttu-id="26ea4-108">En primer lugar, el subproceso maestro utiliza la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear un objeto de evento de restablecimiento manual cuyo estado inicial sea no señalado.</span><span class="sxs-lookup"><span data-stu-id="26ea4-108">First, the master thread uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event object whose initial state is nonsignaled.</span></span> <span data-ttu-id="26ea4-109">Después, crea varios subprocesos de lector.</span><span class="sxs-lookup"><span data-stu-id="26ea4-109">Then it creates several reader threads.</span></span> <span data-ttu-id="26ea4-110">El subproceso maestro realiza una operación de escritura y, a continuación, establece el objeto de evento en el estado señalado cuando ha terminado de escribir.</span><span class="sxs-lookup"><span data-stu-id="26ea4-110">The master thread performs a write operation and then sets the event object to the signaled state when it has finished writing.</span></span>

<span data-ttu-id="26ea4-111">Antes de iniciar una operación de lectura, cada subproceso de lector usa [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para esperar a que se Señalice el objeto de evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="26ea4-111">Before starting a read operation, each reader thread uses [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the manual-reset event object to be signaled.</span></span> <span data-ttu-id="26ea4-112">Cuando **WaitForSingleObject** devuelve, indica que el subproceso principal está listo para que inicie su operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="26ea4-112">When **WaitForSingleObject** returns, this indicates that the main thread is ready for it to begin its read operation.</span></span>


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



 

 
