---
title: Enumerar todos los procesos
description: En el código de ejemplo siguiente se usa la función EnumProcesses para enumerar los procesos actuales del sistema.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89798ed3d2d7e44f014d95833302edb5d5be078daf557eed32d3496c863539e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681012"
---
# <a name="enumerating-all-processes"></a>Enumerar todos los procesos

En el código de ejemplo siguiente se usa [**la función EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) para recuperar el identificador de proceso para cada objeto de proceso del sistema. A continuación, se llama a [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) para obtener cada nombre de proceso e imprimirlo.

>[!NOTE]
> Para procesos de 64 bits, use la [función EnumProcessModulesEx.](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex)

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



La función main obtiene una lista de procesos mediante la [**función EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Para cada proceso, main llama a **la función PrintProcessNameAndID** y le pasa el identificador del proceso. **PrintProcessNameAndID, a su** vez, llama a [**la función OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obtener el identificador del proceso. Si Se produce un error **en OpenProcess,** la salida muestra el nombre del proceso como <unknown> . Por ejemplo, **OpenProcess produce** un error en los procesos Inactivo y CSRSS porque sus restricciones de acceso impiden que el código de nivel de usuario los abra. A **continuación, PrintProcessNameAndID** llama [**a la función EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obtener los identificadores del módulo. Por último, **PrintProcessNameAndID** llama a la función [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) para obtener el nombre del archivo ejecutable y muestra el nombre junto con el identificador del proceso.

 

 
