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
# <a name="creating-threads"></a><span data-ttu-id="09863-103">Crear subprocesos</span><span class="sxs-lookup"><span data-stu-id="09863-103">Creating Threads</span></span>

<span data-ttu-id="09863-104">La función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso.</span><span class="sxs-lookup"><span data-stu-id="09863-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="09863-105">El subproceso de creación debe especificar la dirección inicial del código que va a ejecutar el nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-105">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="09863-106">Normalmente, la dirección de inicio es el nombre de una función definida en el código del programa (para obtener más información, vea [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="09863-106">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="09863-107">Esta función toma un parámetro único y devuelve un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="09863-107">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="09863-108">Un proceso puede tener varios subprocesos que ejecutan simultáneamente la misma función.</span><span class="sxs-lookup"><span data-stu-id="09863-108">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="09863-109">A continuación se muestra un ejemplo sencillo en el que se muestra cómo crear un nuevo subproceso que ejecuta la función definida localmente, `MyThreadFunction` .</span><span class="sxs-lookup"><span data-stu-id="09863-109">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="09863-110">El subproceso que realiza la llamada utiliza la función [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para conservar hasta que todos los subprocesos de trabajo hayan terminado.</span><span class="sxs-lookup"><span data-stu-id="09863-110">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="09863-111">El subproceso que realiza la llamada se bloquea mientras está esperando; para continuar con el procesamiento, un subproceso de llamada usaría [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) y esperar a que cada subproceso de trabajo señale su objeto de espera.</span><span class="sxs-lookup"><span data-stu-id="09863-111">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="09863-112">Tenga en cuenta que si fuera a cerrar el identificador de un subproceso de trabajo antes de finalizar, no finaliza el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="09863-112">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="09863-113">Sin embargo, el identificador no estará disponible para su uso en las siguientes llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="09863-113">However, the handle will be unavailable for use in subsequent function calls.</span></span>


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



<span data-ttu-id="09863-114">La `MyThreadFunction` función evita el uso de la biblioteca en tiempo de ejecución de C (CRT), ya que muchas de sus funciones no son seguras para subprocesos, especialmente si no se usa CRT multiproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-114">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="09863-115">Si desea usar CRT en una `ThreadProc` función, use la función **\_ beginthreadex** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="09863-115">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="09863-116">Es arriesgado pasar la dirección de una variable local si el subproceso de creación sale antes del nuevo subproceso, ya que el puntero deja de ser válido.</span><span class="sxs-lookup"><span data-stu-id="09863-116">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="09863-117">En su lugar, pase un puntero a la memoria asignada dinámicamente o haga que el subproceso de creación espere a que finalice el nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-117">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="09863-118">Los datos también se pueden pasar del subproceso de creación al nuevo subproceso mediante variables globales.</span><span class="sxs-lookup"><span data-stu-id="09863-118">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="09863-119">Con las variables globales, normalmente es necesario sincronizar el acceso de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="09863-119">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="09863-120">Para obtener más información acerca de la sincronización, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="09863-120">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="09863-121">El subproceso de creación puede utilizar los argumentos para [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para especificar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="09863-121">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="09863-122">Los atributos de seguridad para el identificador del nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-122">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="09863-123">Estos atributos de seguridad incluyen una marca de herencia que determina si los procesos secundarios pueden heredar el identificador.</span><span class="sxs-lookup"><span data-stu-id="09863-123">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="09863-124">Los atributos de seguridad también incluyen un descriptor de seguridad, que el sistema utiliza para realizar comprobaciones de acceso en todos los usos subsiguientes del identificador del subproceso antes de que se conceda el acceso.</span><span class="sxs-lookup"><span data-stu-id="09863-124">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="09863-125">Tamaño de pila inicial del nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-125">The initial stack size of the new thread.</span></span> <span data-ttu-id="09863-126">La pila del subproceso se asigna automáticamente en el espacio de memoria del proceso. el sistema aumenta la pila según sea necesario y la libera cuando finaliza el subproceso.</span><span class="sxs-lookup"><span data-stu-id="09863-126">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="09863-127">Para obtener más información, vea [tamaño de pila de subprocesos](thread-stack-size.md).</span><span class="sxs-lookup"><span data-stu-id="09863-127">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="09863-128">Marca de creación que permite crear el subproceso en un estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="09863-128">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="09863-129">Cuando se suspende, el subproceso no se ejecuta hasta que se llama a la función [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="09863-129">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="09863-130">También puede crear un subproceso llamando a la función [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) .</span><span class="sxs-lookup"><span data-stu-id="09863-130">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="09863-131">Esta función la usan los procesos del depurador para crear un subproceso que se ejecuta en el espacio de direcciones del proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="09863-131">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09863-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09863-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09863-133">Finalización de un subproceso</span><span class="sxs-lookup"><span data-stu-id="09863-133">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
