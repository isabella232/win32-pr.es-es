---
title: Enumerar todos los módulos de un proceso
description: Para determinar qué procesos han cargado un archivo DLL determinado, debe enumerar los módulos de cada proceso. En el siguiente código de ejemplo se usa la función EnumProcessModules para enumerar los módulos de los procesos actuales del sistema.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358980"
---
# <a name="enumerating-all-modules-for-a-process"></a><span data-ttu-id="82200-104">Enumerar todos los módulos de un proceso</span><span class="sxs-lookup"><span data-stu-id="82200-104">Enumerating All Modules For a Process</span></span>

<span data-ttu-id="82200-105">Para determinar qué procesos han cargado un archivo DLL determinado, debe enumerar los módulos de cada proceso.</span><span class="sxs-lookup"><span data-stu-id="82200-105">To determine which processes have loaded a particular DLL, you must enumerate the modules for each process.</span></span> <span data-ttu-id="82200-106">En el siguiente código de ejemplo se usa la función [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para enumerar los módulos de los procesos actuales del sistema.</span><span class="sxs-lookup"><span data-stu-id="82200-106">The following sample code uses the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to enumerate the modules of current processes in the system.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



<span data-ttu-id="82200-107">La función Main obtiene una lista de procesos mediante la función [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="82200-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="82200-108">Para cada proceso, la función Main llama a la función PrintModules, pasándole el identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="82200-108">For each process, the main function calls the PrintModules function, passing it the process identifier.</span></span> <span data-ttu-id="82200-109">PrintModules a su vez llama a la función [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obtener el identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="82200-109">PrintModules in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="82200-110">Si se produce un error de **OpenProcess** , la salida muestra solo el identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="82200-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="82200-111">Por ejemplo, se produce un error de **OpenProcess** en los procesos inactivos y csrss porque sus restricciones de acceso impiden que el código de nivel de usuario los abra.</span><span class="sxs-lookup"><span data-stu-id="82200-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="82200-112">A continuación, PrintModules llama a la función [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obtener la función de los identificadores de módulo.</span><span class="sxs-lookup"><span data-stu-id="82200-112">Next, PrintModules calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles function.</span></span> <span data-ttu-id="82200-113">Por último, PrintModules llama a la función [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) , una vez para cada módulo, para obtener los nombres de los módulos.</span><span class="sxs-lookup"><span data-stu-id="82200-113">Finally, PrintModules calls the [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) function, once for each module, to obtain the module names.</span></span>

 

 