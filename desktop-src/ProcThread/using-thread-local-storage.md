---
description: El almacenamiento local de subprocesos (TLS) permite que varios subprocesos del mismo proceso usen un índice asignado por la función TlsAlloc para almacenar y recuperar un valor que sea local para el subproceso.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Uso del almacenamiento local de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9221d4d0d68891ab8e2d0f2462b7c0aae307c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677981"
---
# <a name="using-thread-local-storage"></a><span data-ttu-id="ee5fc-103">Uso del almacenamiento local de subprocesos</span><span class="sxs-lookup"><span data-stu-id="ee5fc-103">Using Thread Local Storage</span></span>

<span data-ttu-id="ee5fc-104">El [almacenamiento local de subprocesos](thread-local-storage.md) (TLS) permite que varios subprocesos del mismo proceso usen un índice asignado por la función [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para almacenar y recuperar un valor que sea local para el subproceso.</span><span class="sxs-lookup"><span data-stu-id="ee5fc-104">[Thread local storage](thread-local-storage.md) (TLS) enables multiple threads of the same process to use an index allocated by the [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to store and retrieve a value that is local to the thread.</span></span> <span data-ttu-id="ee5fc-105">En este ejemplo, se asigna un índice cuando se inicia el proceso.</span><span class="sxs-lookup"><span data-stu-id="ee5fc-105">In this example, an index is allocated when the process starts.</span></span> <span data-ttu-id="ee5fc-106">Cuando cada subproceso se inicia, asigna un bloque de memoria dinámica y almacena un puntero a esta memoria en la ranura TLS mediante la función [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) .</span><span class="sxs-lookup"><span data-stu-id="ee5fc-106">When each thread starts, it allocates a block of dynamic memory and stores a pointer to this memory in the TLS slot using the [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function.</span></span> <span data-ttu-id="ee5fc-107">La función CommonFunc usa la función [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) para tener acceso a los datos asociados al índice que es local para el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="ee5fc-107">The CommonFunc function uses the [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function to access the data associated with the index that is local to the calling thread.</span></span> <span data-ttu-id="ee5fc-108">Antes de que finalice cada subproceso, libera su memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="ee5fc-108">Before each thread terminates, it releases its dynamic memory.</span></span> <span data-ttu-id="ee5fc-109">Antes de que finalice el proceso, llama a [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar el índice.</span><span class="sxs-lookup"><span data-stu-id="ee5fc-109">Before the process terminates, it calls [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) to release the index.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
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
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="ee5fc-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee5fc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee5fc-111">Usar el almacenamiento local para el subproceso en una biblioteca de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="ee5fc-111">Using Thread Local Storage in a Dynamic-Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
