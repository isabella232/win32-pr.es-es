---
description: En esta sección se muestra el uso de una función de punto de entrada dll para configurar un índice de almacenamiento local de subprocesos (TLS) para proporcionar almacenamiento privado para cada subproceso de un proceso multiproceso.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Uso de subprocesos Storage en una biblioteca Dynamic-Link subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44aaf4a4f5314539d788f4558548c110259bd49c40807a07603e432d3f468c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902325"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Uso de subprocesos Storage en una biblioteca Dynamic-Link subprocesos

En esta sección se muestra el uso de una función de punto de entrada dll para configurar un índice de almacenamiento local de subprocesos (TLS) para proporcionar almacenamiento privado para cada subproceso de un proceso multiproceso.

El índice TLS se almacena en una variable global, lo que lo hace disponible para todas las funciones DLL. En este ejemplo se da por supuesto que los datos globales del archivo DLL no se comparten, ya que el índice TLS no es necesariamente el mismo para cada proceso que carga el archivo DLL.

La función de punto de entrada usa la [**función TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS cada vez que un proceso carga el archivo DLL. A continuación, cada subproceso puede usar este índice para almacenar un puntero a su propio bloque de memoria.

Cuando se llama a la función de punto de entrada con el valor DLL PROCESS ATTACH, el código \_ \_ realiza las siguientes acciones:

1.  Usa la [**función TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS.
2.  Asigna un bloque de memoria que el subproceso inicial del proceso usará exclusivamente.
3.  Usa el índice TLS en una llamada a la función [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) para almacenar la dirección del bloque de memoria en la ranura TLS asociada al índice.

Cada vez que el proceso crea un subproceso, se llama a la función de punto de entrada con el valor \_ ATTACH \_ de DLL THREAD. A continuación, la función de punto de entrada asigna un bloque de memoria para el nuevo subproceso y almacena un puntero a él mediante el índice TLS.

Cuando una función requiere acceso a los datos asociados a un índice TLS, especifique el índice en una llamada a la [**función TlsGetValue.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) Esto recupera el contenido de la ranura TLS para el subproceso que realiza la llamada, que en este caso es un puntero al bloque de memoria de los datos. Cuando un proceso usa la vinculación en tiempo de carga con este archivo DLL, la función de punto de entrada es suficiente para administrar el almacenamiento local del subproceso. Pueden producirse problemas con un proceso que usa la vinculación en tiempo de ejecución porque no se llama a la función de punto de entrada para los subprocesos que existen antes de llamar a la función [**LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) por lo que no se asigna memoria TLS para estos subprocesos. En este ejemplo se resuelve este problema comprobando el valor devuelto por la función [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) y asignando memoria si el valor indica que no se ha establecido la ranura TLS para este subproceso.

Cuando cada subproceso ya no necesita usar un índice TLS, debe liberar la memoria cuyo puntero se almacena en la ranura TLS. Cuando todos los subprocesos terminen de usar un índice TLS, use la [**función TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar el índice.

Cuando finaliza un subproceso, se llama a la función de punto de entrada con el valor DLL THREAD DETACH y se libera la \_ \_ memoria de ese subproceso. Cuando finaliza un proceso, se llama a la función de punto de entrada con el valor DETACH DE DLL PROCESS y se libera la memoria a la que hace referencia el puntero en el \_ \_ índice TLS.


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



El código siguiente muestra el uso de las funciones DLL definidas en el ejemplo anterior.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos de la biblioteca de vínculos dinámicos](dynamic-link-library-data.md)
</dt> <dt>

[Uso del almacenamiento local de subprocesos](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
