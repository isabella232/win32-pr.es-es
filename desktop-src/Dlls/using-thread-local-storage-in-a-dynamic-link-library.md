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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Usar el almacenamiento local para el subproceso en una biblioteca de Dynamic-Link

En esta sección se muestra el uso de una función de punto de entrada de DLL para configurar un índice de almacenamiento local de subprocesos (TLS) para proporcionar almacenamiento privado para cada subproceso de un proceso multiproceso.

El índice TLS se almacena en una variable global y lo pone a disposición de todas las funciones DLL. En este ejemplo se da por supuesto que los datos globales del archivo DLL no están compartidos, ya que el índice TLS no es necesariamente el mismo para cada proceso que carga el archivo DLL.

La función de punto de entrada utiliza la función [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS cada vez que un proceso carga el archivo dll. A continuación, cada subproceso puede utilizar este índice para almacenar un puntero a su propio bloque de memoria.

Cuando se llama a la función de punto de entrada con el \_ valor Attach del proceso de dll \_ , el código realiza las siguientes acciones:

1.  Utiliza la función [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice TLS.
2.  Asigna un bloque de memoria que va a usar exclusivamente el subproceso inicial del proceso.
3.  Usa el índice TLS en una llamada a la función [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) para almacenar la dirección del bloque de memoria en la ranura TLS asociada al índice.

Cada vez que el proceso crea un nuevo subproceso, se llama a la función de punto de entrada con el \_ valor Attach del subproceso de la dll \_ . A continuación, la función de punto de entrada asigna un bloque de memoria para el nuevo subproceso y almacena un puntero a él mediante el índice de TLS.

Cuando una función requiere acceso a los datos asociados a un índice TLS, especifique el índice en una llamada a la función [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) . Esto recupera el contenido de la ranura TLS para el subproceso que realiza la llamada, que en este caso es un puntero al bloque de memoria para los datos. Cuando un proceso usa la vinculación en tiempo de carga con este archivo DLL, la función de punto de entrada es suficiente para administrar el almacenamiento local del subproceso. Pueden producirse problemas con un proceso que usa la vinculación en tiempo de ejecución porque no se llama a la función de punto de entrada para los subprocesos que existen antes de que se llame a la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , por lo que no se asigna la memoria TLS para estos subprocesos. Este ejemplo resuelve este problema comprobando el valor devuelto por la función [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) y asignando memoria si el valor indica que no se ha establecido la ranura TLS para este subproceso.

Cuando cada subproceso ya no necesita usar un índice TLS, debe liberar la memoria cuyo puntero se almacena en la ranura TLS. Cuando todos los subprocesos hayan terminado de usar un índice TLS, utilice la función [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar el índice.

Cuando finaliza un subproceso, se llama a la función de punto de entrada con el \_ valor de separación de subprocesos \_ de dll y se libera la memoria para ese subproceso. Cuando finaliza un proceso, se llama a la función de punto de entrada con el \_ \_ valor de desasociación del proceso de dll y se libera la memoria a la que hace referencia el puntero en el índice de TLS.


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



En el código siguiente se muestra el uso de las funciones DLL definidas en el ejemplo anterior.


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

[Datos de biblioteca de vínculos dinámicos](dynamic-link-library-data.md)
</dt> <dt>

[Uso del almacenamiento local de subprocesos](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
