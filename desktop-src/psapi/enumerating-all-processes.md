---
title: Enumerar todos los procesos
description: En el código de ejemplo siguiente se usa la función EnumProcesses para enumerar los procesos actuales del sistema.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03fd9ad06bfb15924f3f5ec92d8f8858fbff60
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644117"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="f1179-103">Enumerar todos los procesos</span><span class="sxs-lookup"><span data-stu-id="f1179-103">Enumerating All Processes</span></span>

<span data-ttu-id="f1179-104">En el código de ejemplo siguiente se usa [**la función EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) para recuperar el identificador de proceso para cada objeto de proceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="f1179-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="f1179-105">A continuación, se llama a [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) para obtener el nombre de cada proceso e imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="f1179-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="f1179-106">Para procesos de 64 bits, use la [función EnumProcessModulesEx.](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex)</span><span class="sxs-lookup"><span data-stu-id="f1179-106">For 64 bit processes, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="f1179-107">La función main obtiene una lista de procesos mediante la [**función EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)</span><span class="sxs-lookup"><span data-stu-id="f1179-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="f1179-108">Para cada proceso, main llama a **la función PrintProcessNameAndID** y le pasa el identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="f1179-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="f1179-109">**PrintProcessNameAndID a** su vez llama a [**la función OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obtener el identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="f1179-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="f1179-110">Si se produce un error **en OpenProcess,** la salida muestra el nombre del proceso como <unknown> .</span><span class="sxs-lookup"><span data-stu-id="f1179-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="f1179-111">Por ejemplo, **OpenProcess** produce un error en los procesos Inactivo y CSRSS porque sus restricciones de acceso impiden que el código de nivel de usuario los abra.</span><span class="sxs-lookup"><span data-stu-id="f1179-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="f1179-112">A **continuación, PrintProcessNameAndID** llama [**a la función EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obtener los identificadores del módulo.</span><span class="sxs-lookup"><span data-stu-id="f1179-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="f1179-113">Por último, **PrintProcessNameAndID** llama a la función [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) para obtener el nombre del archivo ejecutable y muestra el nombre junto con el identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="f1179-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
