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
# <a name="using-shared-memory-in-a-dynamic-link-library"></a><span data-ttu-id="8adde-103">Uso de memoria compartida en una biblioteca de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="8adde-103">Using Shared Memory in a Dynamic-Link Library</span></span>

<span data-ttu-id="8adde-104">En el ejemplo siguiente se muestra cómo la función de punto de entrada de DLL puede utilizar un objeto de asignación de archivos para configurar la memoria que pueden compartir los procesos que cargan el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="8adde-104">The following example demonstrates how the DLL entry-point function can use a file-mapping object to set up memory that can be shared by processes that load the DLL.</span></span> <span data-ttu-id="8adde-105">La memoria DLL compartida se conserva solo mientras se carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="8adde-105">The shared DLL memory persists only as long as the DLL is loaded.</span></span> <span data-ttu-id="8adde-106">Las aplicaciones pueden usar las funciones SetSharedMem y GetSharedMem para tener acceso a la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="8adde-106">Applications can use the SetSharedMem and GetSharedMem functions to access the shared memory.</span></span>

## <a name="dll-that-implements-the-shared-memory"></a><span data-ttu-id="8adde-107">DLL que implementa la memoria compartida</span><span class="sxs-lookup"><span data-stu-id="8adde-107">DLL that Implements the Shared Memory</span></span>

<span data-ttu-id="8adde-108">En el ejemplo se usa la asignación de archivos para asignar un bloque de memoria compartida con nombre en el espacio de direcciones virtuales de cada proceso que carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="8adde-108">The example uses file mapping to map a block of named shared memory into the virtual address space of each process that loads the DLL.</span></span> <span data-ttu-id="8adde-109">Para ello, la función de punto de entrada debe:</span><span class="sxs-lookup"><span data-stu-id="8adde-109">To do this, the entry-point function must:</span></span>

1.  <span data-ttu-id="8adde-110">Llame a la función [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) para obtener un identificador de un objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8adde-110">Call the [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) function to get a handle to a file-mapping object.</span></span> <span data-ttu-id="8adde-111">El primer proceso que carga el archivo DLL crea el objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8adde-111">The first process that loads the DLL creates the file-mapping object.</span></span> <span data-ttu-id="8adde-112">Los procesos posteriores abren un identificador para el objeto existente.</span><span class="sxs-lookup"><span data-stu-id="8adde-112">Subsequent processes open a handle to the existing object.</span></span> <span data-ttu-id="8adde-113">Para obtener más información, vea [crear un objeto de File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).</span><span class="sxs-lookup"><span data-stu-id="8adde-113">For more information, see [Creating a File-Mapping Object](/windows/desktop/Memory/creating-a-file-mapping-object).</span></span>
2.  <span data-ttu-id="8adde-114">Llame a la función [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) para asignar una vista en el espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="8adde-114">Call the [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) function to map a view into the virtual address space.</span></span> <span data-ttu-id="8adde-115">Esto permite que el proceso tenga acceso a la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="8adde-115">This enables the process to access the shared memory.</span></span> <span data-ttu-id="8adde-116">Para obtener más información, consulte [crear una vista de archivo](/windows/desktop/Memory/creating-a-file-view).</span><span class="sxs-lookup"><span data-stu-id="8adde-116">For more information, see [Creating a File View](/windows/desktop/Memory/creating-a-file-view).</span></span>

<span data-ttu-id="8adde-117">Tenga en cuenta que, aunque puede especificar los atributos de seguridad predeterminados pasando un valor NULL para el parámetro *lpAttributes* de [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), puede optar por usar una estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para proporcionar seguridad adicional.</span><span class="sxs-lookup"><span data-stu-id="8adde-117">Note that while you can specify default security attributes by passing in a NULL value for the *lpAttributes* parameter of [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), you may choose to use a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to provide additional security.</span></span>


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



<span data-ttu-id="8adde-118">La memoria compartida se puede asignar a una dirección diferente en cada proceso.</span><span class="sxs-lookup"><span data-stu-id="8adde-118">Shared memory can be mapped to a different address in each process.</span></span> <span data-ttu-id="8adde-119">Por esta razón, cada proceso tiene su propia instancia de lpvMem, que se declara como una variable global para que esté disponible para todas las funciones DLL.</span><span class="sxs-lookup"><span data-stu-id="8adde-119">For this reason, each process has its own instance of lpvMem, which is declared as a global variable so that it is available to all DLL functions.</span></span> <span data-ttu-id="8adde-120">En el ejemplo se supone que los datos globales de la DLL no están compartidos, por lo que cada proceso que carga el archivo DLL tiene su propia instancia de lpvMem.</span><span class="sxs-lookup"><span data-stu-id="8adde-120">The example assumes that the DLL global data is not shared, so each process that loads the DLL has its own instance of lpvMem.</span></span>

<span data-ttu-id="8adde-121">Tenga en cuenta que la memoria compartida se libera cuando se cierra el último identificador del objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8adde-121">Note that the shared memory is released when the last handle to the file-mapping object is closed.</span></span> <span data-ttu-id="8adde-122">Para crear memoria compartida persistente, tendría que asegurarse de que algún proceso tenga siempre un identificador abierto para el objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8adde-122">To create persistent shared memory, you would need to ensure that some process always has an open handle to the file-mapping object.</span></span>

## <a name="processes-that-use-the-shared-memory"></a><span data-ttu-id="8adde-123">Procesos que usan la memoria compartida</span><span class="sxs-lookup"><span data-stu-id="8adde-123">Processes that Use the Shared Memory</span></span>

<span data-ttu-id="8adde-124">Los siguientes procesos utilizan la memoria compartida proporcionada por el archivo DLL definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8adde-124">The following processes use the shared memory provided by the DLL defined above.</span></span> <span data-ttu-id="8adde-125">El primer proceso llama a SetSharedMem para escribir una cadena mientras que el segundo proceso llama a GetSharedMem para recuperar esta cadena.</span><span class="sxs-lookup"><span data-stu-id="8adde-125">The first process calls SetSharedMem to write a string while the second process calls GetSharedMem to retrieve this string.</span></span>

<span data-ttu-id="8adde-126">Este proceso usa la función SetSharedMem implementada por el archivo DLL para escribir la cadena "This is a Test String" en la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="8adde-126">This process uses the SetSharedMem function implemented by the DLL to write the string "This is a test string" to the shared memory.</span></span> <span data-ttu-id="8adde-127">También inicia un proceso secundario que leerá la cadena de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="8adde-127">It also starts a child process that will read the string from the shared memory.</span></span>


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



<span data-ttu-id="8adde-128">Este proceso usa la función GetSharedMem implementada por el archivo DLL para leer una cadena de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="8adde-128">This process uses the GetSharedMem function implemented by the DLL to read a string from the shared memory.</span></span> <span data-ttu-id="8adde-129">Lo inicia el proceso primario anterior.</span><span class="sxs-lookup"><span data-stu-id="8adde-129">It is started by the parent process above.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8adde-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8adde-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8adde-131">Datos de biblioteca de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="8adde-131">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> </dl>

 

 
