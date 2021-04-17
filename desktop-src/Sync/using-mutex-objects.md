---
description: Puede usar un objeto mutex para proteger un recurso compartido de un acceso simultáneo de varios subprocesos o procesos.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Usar objetos mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667502"
---
# <a name="using-mutex-objects"></a><span data-ttu-id="142dd-103">Usar objetos mutex</span><span class="sxs-lookup"><span data-stu-id="142dd-103">Using Mutex Objects</span></span>

<span data-ttu-id="142dd-104">Puede usar un [objeto mutex](mutex-objects.md) para proteger un recurso compartido de un acceso simultáneo de varios subprocesos o procesos.</span><span class="sxs-lookup"><span data-stu-id="142dd-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="142dd-105">Cada subproceso debe esperar a la propiedad de la exclusión mutua para poder ejecutar el código que tiene acceso al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="142dd-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="142dd-106">Por ejemplo, si varios subprocesos comparten el acceso a una base de datos, los subprocesos pueden utilizar un objeto mutex para permitir que solo un subproceso cada vez escriba en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="142dd-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="142dd-107">En el ejemplo siguiente se usa la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para crear un objeto mutex y la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para crear subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="142dd-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="142dd-108">Cuando un subproceso de este proceso escribe en la base de datos, primero solicita la propiedad de la exclusión mutua mediante la función [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="142dd-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="142dd-109">Si el subproceso obtiene la propiedad de la exclusión mutua, escribe en la base de datos y, a continuación, libera su propiedad de la exclusión mutua mediante la función [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .</span><span class="sxs-lookup"><span data-stu-id="142dd-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="142dd-110">En este ejemplo se usa el control de excepciones estructurado para asegurarse de que el subproceso libera correctamente el objeto mutex.</span><span class="sxs-lookup"><span data-stu-id="142dd-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="142dd-111">El bloque de código **\_ \_ Finally** se ejecuta independientemente de cómo finalice el bloque **\_ \_ try** (a menos que el bloque **\_ \_ try** incluya una llamada a la función [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ).</span><span class="sxs-lookup"><span data-stu-id="142dd-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="142dd-112">Esto evita que el objeto mutex se abandone accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="142dd-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="142dd-113">Si se abandona una exclusión mutua, el subproceso que poseía la exclusión mutua no la liberaba correctamente antes de finalizar.</span><span class="sxs-lookup"><span data-stu-id="142dd-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="142dd-114">En este caso, el estado del recurso compartido es indeterminado y seguir usando la exclusión mutua puede ocultar un error potencialmente grave.</span><span class="sxs-lookup"><span data-stu-id="142dd-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="142dd-115">Es posible que algunas aplicaciones intenten restaurar el recurso a un estado coherente. en este ejemplo se devuelve simplemente un error y se detiene el uso de la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="142dd-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="142dd-116">Para obtener más información, vea [objetos mutex](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="142dd-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
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

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
