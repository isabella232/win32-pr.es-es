---
title: Enumerar todos los módulos de un proceso
description: Para determinar qué procesos han cargado un archivo DLL determinado, debe enumerar los módulos de cada proceso. El código de ejemplo siguiente usa la función EnumProcessModules para enumerar los módulos de los procesos actuales del sistema.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17012019c21f550940ea8c11c07153b0c3495471b4d62bf2f8af469ef6b7b90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032993"
---
# <a name="enumerating-all-modules-for-a-process"></a>Enumerar todos los módulos de un proceso

Para determinar qué procesos han cargado un archivo DLL determinado, debe enumerar los módulos de cada proceso. El código de ejemplo siguiente usa la [**función EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para enumerar los módulos de los procesos actuales del sistema.


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



La función main obtiene una lista de procesos mediante la [**función EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Para cada proceso, la función principal llama a la función PrintModules y le pasa el identificador del proceso. PrintModules, a su vez, llama [**a la función OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obtener el identificador del proceso. Si Se produce un error **en OpenProcess,** la salida muestra solo el identificador del proceso. Por ejemplo, **OpenProcess produce** un error en los procesos Inactivo y CSRSS porque sus restricciones de acceso impiden que el código de nivel de usuario los abra. A continuación, PrintModules llama [**a la función EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obtener la función de identificadores de módulo. Por último, PrintModules llama a [**la función GetModuleFileNameEx,**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) una vez para cada módulo, para obtener los nombres de módulo.

 

 