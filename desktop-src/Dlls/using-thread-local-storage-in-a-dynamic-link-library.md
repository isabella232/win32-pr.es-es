---
description: En esta sección se muestra el uso de una función de punto de entrada de DLL para configurar un índice de almacenamiento local de subprocesos (TLS) para proporcionar almacenamiento privado para cada subproceso de un proceso multiproceso.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Usar el almacenamiento local para el subproceso en una biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687142"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="b4e40-103">Usar el almacenamiento local para el subproceso en una biblioteca de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="b4e40-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="b4e40-104">En esta sección se muestra el uso de una función de punto de entrada de DLL para configurar un índice de almacenamiento local de subprocesos (TLS) para proporcionar almacenamiento privado para cada subproceso de un proceso multiproceso.</span><span class="sxs-lookup"><span data-stu-id="b4e40-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="b4e40-105">El índice TLS se almacena en una variable global y lo pone a disposición de todas las funciones DLL.</span><span class="sxs-lookup"><span data-stu-id="b4e40-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="b4e40-106">En este ejemplo se da por supuesto que los datos globales del archivo DLL no están compartidos, ya que el índice TLS no es necesariamente el mismo para cada proceso que carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b4e40-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="b4e40-107">La función de punto de entrada utiliza la función [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS cada vez que un proceso carga el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="b4e40-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="b4e40-108">A continuación, cada subproceso puede utilizar este índice para almacenar un puntero a su propio bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="b4e40-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="b4e40-109">Cuando se llama a la función de punto de entrada con el \_ valor Attach del proceso de dll \_ , el código realiza las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="b4e40-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="b4e40-110">Utiliza la función [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS.</span><span class="sxs-lookup"><span data-stu-id="b4e40-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="b4e40-111">Asigna un bloque de memoria que va a usar exclusivamente el subproceso inicial del proceso.</span><span class="sxs-lookup"><span data-stu-id="b4e40-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="b4e40-112">Usa el índice TLS en una llamada a la función [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) para almacenar la dirección del bloque de memoria en la ranura TLS asociada al índice.</span><span class="sxs-lookup"><span data-stu-id="b4e40-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="b4e40-113">Cada vez que el proceso crea un nuevo subproceso, se llama a la función de punto de entrada con el \_ valor Attach del subproceso de la dll \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e40-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="b4e40-114">A continuación, la función de punto de entrada asigna un bloque de memoria para el nuevo subproceso y almacena un puntero a él mediante el índice de TLS.</span><span class="sxs-lookup"><span data-stu-id="b4e40-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="b4e40-115">Cuando una función requiere acceso a los datos asociados a un índice TLS, especifique el índice en una llamada a la función [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) .</span><span class="sxs-lookup"><span data-stu-id="b4e40-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="b4e40-116">Esto recupera el contenido de la ranura TLS para el subproceso que realiza la llamada, que en este caso es un puntero al bloque de memoria para los datos.</span><span class="sxs-lookup"><span data-stu-id="b4e40-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="b4e40-117">Cuando un proceso usa la vinculación en tiempo de carga con este archivo DLL, la función de punto de entrada es suficiente para administrar el almacenamiento local del subproceso.</span><span class="sxs-lookup"><span data-stu-id="b4e40-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="b4e40-118">Pueden producirse problemas con un proceso que usa la vinculación en tiempo de ejecución porque no se llama a la función de punto de entrada para los subprocesos que existen antes de que se llame a la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , por lo que no se asigna la memoria TLS para estos subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b4e40-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="b4e40-119">Este ejemplo resuelve este problema comprobando el valor devuelto por la función [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) y asignando memoria si el valor indica que no se ha establecido la ranura TLS para este subproceso.</span><span class="sxs-lookup"><span data-stu-id="b4e40-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="b4e40-120">Cuando cada subproceso ya no necesita usar un índice TLS, debe liberar la memoria cuyo puntero se almacena en la ranura TLS.</span><span class="sxs-lookup"><span data-stu-id="b4e40-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="b4e40-121">Cuando todos los subprocesos hayan terminado de usar un índice TLS, utilice la función [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar el índice.</span><span class="sxs-lookup"><span data-stu-id="b4e40-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="b4e40-122">Cuando finaliza un subproceso, se llama a la función de punto de entrada con el \_ valor de separación de subprocesos \_ de dll y se libera la memoria para ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="b4e40-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="b4e40-123">Cuando finaliza un proceso, se llama a la función de punto de entrada con el \_ \_ valor de desasociación del proceso de dll y se libera la memoria a la que hace referencia el puntero en el índice de TLS.</span><span class="sxs-lookup"><span data-stu-id="b4e40-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="b4e40-124">En el código siguiente se muestra el uso de las funciones DLL definidas en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="b4e40-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="b4e40-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4e40-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4e40-126">Datos de biblioteca de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="b4e40-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="b4e40-127">Uso del almacenamiento local de subprocesos</span><span class="sxs-lookup"><span data-stu-id="b4e40-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
