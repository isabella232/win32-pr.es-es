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
# <a name="using-mutex-objects"></a>Usar objetos mutex

Puede usar un [objeto mutex](mutex-objects.md) para proteger un recurso compartido de un acceso simultáneo de varios subprocesos o procesos. Cada subproceso debe esperar a la propiedad de la exclusión mutua para poder ejecutar el código que tiene acceso al recurso compartido. Por ejemplo, si varios subprocesos comparten el acceso a una base de datos, los subprocesos pueden utilizar un objeto mutex para permitir que solo un subproceso cada vez escriba en la base de datos.

En el ejemplo siguiente se usa la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para crear un objeto mutex y la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para crear subprocesos de trabajo.

Cuando un subproceso de este proceso escribe en la base de datos, primero solicita la propiedad de la exclusión mutua mediante la función [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) . Si el subproceso obtiene la propiedad de la exclusión mutua, escribe en la base de datos y, a continuación, libera su propiedad de la exclusión mutua mediante la función [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .

En este ejemplo se usa el control de excepciones estructurado para asegurarse de que el subproceso libera correctamente el objeto mutex. El bloque de código **\_ \_ Finally** se ejecuta independientemente de cómo finalice el bloque **\_ \_ try** (a menos que el bloque **\_ \_ try** incluya una llamada a la función [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ). Esto evita que el objeto mutex se abandone accidentalmente.

Si se abandona una exclusión mutua, el subproceso que poseía la exclusión mutua no la liberaba correctamente antes de finalizar. En este caso, el estado del recurso compartido es indeterminado y seguir usando la exclusión mutua puede ocultar un error potencialmente grave. Es posible que algunas aplicaciones intenten restaurar el recurso a un estado coherente. en este ejemplo se devuelve simplemente un error y se detiene el uso de la exclusión mutua. Para obtener más información, vea [objetos mutex](mutex-objects.md).


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



 

 
