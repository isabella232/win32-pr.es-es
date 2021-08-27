---
description: El almacenamiento local de subprocesos (TLS) permite que varios subprocesos del mismo proceso usen un índice asignado por la función TlsAlloc para almacenar y recuperar un valor local para el subproceso.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Uso del almacenamiento local de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdac1306a4a2da10e6a24ba2e1b2444f6215fdac39be7b41cc6850c1e5a683d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127995"
---
# <a name="using-thread-local-storage"></a>Uso del almacenamiento local de subprocesos

[El almacenamiento local de](thread-local-storage.md) subprocesos (TLS) permite que varios subprocesos del mismo proceso usen un índice asignado por la [**función TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para almacenar y recuperar un valor local para el subproceso. En este ejemplo, se asigna un índice cuando se inicia el proceso. Cuando se inicia cada subproceso, asigna un bloque de memoria dinámica y almacena un puntero a esta memoria en la ranura TLS mediante la [**función TlsSetValue.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) La función CommonFunc usa la [**función TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) para tener acceso a los datos asociados al índice que es local para el subproceso que realiza la llamada. Antes de que finalice cada subproceso, libera su memoria dinámica. Antes de que finalice el proceso, llama a [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar el índice.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de subprocesos Storage local en una biblioteca Dynamic-Link de subprocesos](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
