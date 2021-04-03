---
description: En el ejemplo siguiente se muestra cómo la función de punto de entrada de DLL puede utilizar un objeto de asignación de archivos para configurar la memoria que pueden compartir los procesos que cargan el archivo DLL.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Uso de memoria compartida en una biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908352"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Uso de memoria compartida en una biblioteca de Dynamic-Link

En el ejemplo siguiente se muestra cómo la función de punto de entrada de DLL puede utilizar un objeto de asignación de archivos para configurar la memoria que pueden compartir los procesos que cargan el archivo DLL. La memoria DLL compartida se conserva solo mientras se carga el archivo DLL. Las aplicaciones pueden usar las funciones SetSharedMem y GetSharedMem para tener acceso a la memoria compartida.

## <a name="dll-that-implements-the-shared-memory"></a>DLL que implementa la memoria compartida

En el ejemplo se usa la asignación de archivos para asignar un bloque de memoria compartida con nombre en el espacio de direcciones virtuales de cada proceso que carga el archivo DLL. Para ello, la función de punto de entrada debe:

1.  Llame a la función [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) para obtener un identificador de un objeto de asignación de archivos. El primer proceso que carga el archivo DLL crea el objeto de asignación de archivos. Los procesos posteriores abren un identificador para el objeto existente. Para obtener más información, vea [crear un objeto de File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Llame a la función [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar una vista en el espacio de direcciones virtuales. Esto permite que el proceso tenga acceso a la memoria compartida. Para obtener más información, consulte [crear una vista de archivo](/windows/desktop/Memory/creating-a-file-view).

Tenga en cuenta que, aunque puede especificar los atributos de seguridad predeterminados pasando un valor NULL para el parámetro *lpAttributes* de [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), puede optar por usar una estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para proporcionar seguridad adicional.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



La memoria compartida se puede asignar a una dirección diferente en cada proceso. Por esta razón, cada proceso tiene su propia instancia de lpvMem, que se declara como una variable global para que esté disponible para todas las funciones DLL. En el ejemplo se supone que los datos globales de la DLL no están compartidos, por lo que cada proceso que carga el archivo DLL tiene su propia instancia de lpvMem.

Tenga en cuenta que la memoria compartida se libera cuando se cierra el último identificador del objeto de asignación de archivos. Para crear memoria compartida persistente, tendría que asegurarse de que algún proceso tenga siempre un identificador abierto para el objeto de asignación de archivos.

## <a name="processes-that-use-the-shared-memory"></a>Procesos que usan la memoria compartida

Los siguientes procesos utilizan la memoria compartida proporcionada por el archivo DLL definido anteriormente. El primer proceso llama a SetSharedMem para escribir una cadena mientras que el segundo proceso llama a GetSharedMem para recuperar esta cadena.

Este proceso usa la función SetSharedMem implementada por el archivo DLL para escribir la cadena "This is a Test String" en la memoria compartida. También inicia un proceso secundario que leerá la cadena de la memoria compartida.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



Este proceso usa la función GetSharedMem implementada por el archivo DLL para leer una cadena de la memoria compartida. Lo inicia el proceso primario anterior.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos de biblioteca de vínculos dinámicos](dynamic-link-library-data.md)
</dt> </dl>

 

 
