---
description: La función CreateThread crea un nuevo subproceso para un proceso.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Crear subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545088779bdaff665a8079296014535ab244e821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677864"
---
# <a name="creating-threads"></a>Crear subprocesos

La función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso. El subproceso de creación debe especificar la dirección inicial del código que va a ejecutar el nuevo subproceso. Normalmente, la dirección de inicio es el nombre de una función definida en el código del programa (para obtener más información, vea [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Esta función toma un parámetro único y devuelve un valor **DWORD** . Un proceso puede tener varios subprocesos que ejecutan simultáneamente la misma función.

A continuación se muestra un ejemplo sencillo en el que se muestra cómo crear un nuevo subproceso que ejecuta la función definida localmente, `MyThreadFunction` .

El subproceso que realiza la llamada utiliza la función [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para conservar hasta que todos los subprocesos de trabajo hayan terminado. El subproceso que realiza la llamada se bloquea mientras está esperando; para continuar con el procesamiento, un subproceso de llamada usaría [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) y esperar a que cada subproceso de trabajo señale su objeto de espera. Tenga en cuenta que si fuera a cerrar el identificador de un subproceso de trabajo antes de finalizar, no finaliza el subproceso de trabajo. Sin embargo, el identificador no estará disponible para su uso en las siguientes llamadas de función.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



La `MyThreadFunction` función evita el uso de la biblioteca en tiempo de ejecución de C (CRT), ya que muchas de sus funciones no son seguras para subprocesos, especialmente si no se usa CRT multiproceso. Si desea usar CRT en una `ThreadProc` función, use la función **\_ beginthreadex** en su lugar.

Es arriesgado pasar la dirección de una variable local si el subproceso de creación sale antes del nuevo subproceso, ya que el puntero deja de ser válido. En su lugar, pase un puntero a la memoria asignada dinámicamente o haga que el subproceso de creación espere a que finalice el nuevo subproceso. Los datos también se pueden pasar del subproceso de creación al nuevo subproceso mediante variables globales. Con las variables globales, normalmente es necesario sincronizar el acceso de varios subprocesos. Para obtener más información acerca de la sincronización, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).

El subproceso de creación puede utilizar los argumentos para [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para especificar lo siguiente:

-   Los atributos de seguridad para el identificador del nuevo subproceso. Estos atributos de seguridad incluyen una marca de herencia que determina si los procesos secundarios pueden heredar el identificador. Los atributos de seguridad también incluyen un descriptor de seguridad, que el sistema utiliza para realizar comprobaciones de acceso en todos los usos subsiguientes del identificador del subproceso antes de que se conceda el acceso.
-   Tamaño de pila inicial del nuevo subproceso. La pila del subproceso se asigna automáticamente en el espacio de memoria del proceso. el sistema aumenta la pila según sea necesario y la libera cuando finaliza el subproceso. Para obtener más información, vea [tamaño de pila de subprocesos](thread-stack-size.md).
-   Marca de creación que permite crear el subproceso en un estado suspendido. Cuando se suspende, el subproceso no se ejecuta hasta que se llama a la función [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .

También puede crear un subproceso llamando a la función [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Esta función la usan los procesos del depurador para crear un subproceso que se ejecuta en el espacio de direcciones del proceso que se está depurando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Finalización de un subproceso](terminating-a-thread.md)
</dt> </dl>

 

 
