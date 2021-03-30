---
description: La función CreateProcess crea un nuevo proceso, que se ejecuta independientemente del proceso de creación. Sin embargo, para simplificar, la relación se conoce como una relación de elementos primarios y secundarios.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Crear procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001944"
---
# <a name="creating-processes"></a><span data-ttu-id="a0a0c-104">Crear procesos</span><span class="sxs-lookup"><span data-stu-id="a0a0c-104">Creating Processes</span></span>

<span data-ttu-id="a0a0c-105">La función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crea un nuevo proceso, que se ejecuta independientemente del proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="a0a0c-106">Sin embargo, para simplificar, la relación se conoce como una relación de elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="a0a0c-107">En el código siguiente se muestra cómo crear un proceso.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-107">The following code demonstrates how to create a process.</span></span>


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



<span data-ttu-id="a0a0c-108">Si [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) se ejecuta correctamente, devuelve una estructura de [**\_ información de proceso**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) que contiene identificadores e identificadores para el nuevo proceso y su subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="a0a0c-109">Los identificadores de subprocesos y procesos se crean con derechos de acceso completo, aunque el acceso se puede restringir si se especifican descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="a0a0c-110">Cuando ya no necesite estos identificadores, ciérrelo mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="a0a0c-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="a0a0c-111">También puede crear un proceso mediante la función [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) .</span><span class="sxs-lookup"><span data-stu-id="a0a0c-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="a0a0c-112">Esto le permite especificar el contexto de seguridad de la cuenta de usuario en la que se ejecutará el proceso.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
