---
description: La función CreateProcess crea un nuevo proceso, que se ejecuta independientemente del proceso de creación. Sin embargo, para simplificar, la relación se conoce como relación de elementos primarios y secundarios.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Crear procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8e5e4340f5c956e964b74ab134a7618a4c4bf0fa44eee1989a0457741d7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143108"
---
# <a name="creating-processes"></a>Crear procesos

La [**función CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crea un nuevo proceso, que se ejecuta independientemente del proceso de creación. Sin embargo, para simplificar, la relación se conoce como relación de elementos primarios y secundarios.

En el código siguiente se muestra cómo crear un proceso.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



Si [**CreateProcess se**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) realiza correctamente, devuelve una estructura [**PROCESS \_ INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) que contiene identificadores y identificadores para el nuevo proceso y su subproceso principal. Los identificadores de subproceso y proceso se crean con derechos de acceso completos, aunque el acceso se puede restringir si se especifican descriptores de seguridad. Cuando ya no necesite estos identificadores, conéctelos mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

También puede crear un proceso mediante las [**funciones CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) [**o CreateProcessWithLogonW.**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) Esto le permite especificar el contexto de seguridad de la cuenta de usuario en la que se ejecutará el proceso.

 

 
