---
title: Tomar una instantánea y ver los procesos
description: La siguiente aplicación de consola sencilla obtiene una lista de procesos en ejecución.
ms.assetid: 318d166f-858f-4f33-9422-977e0c4beb3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90a90ea3456d2783c6015ae230d0f0b9e84806e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685758"
---
# <a name="taking-a-snapshot-and-viewing-processes"></a><span data-ttu-id="6aab8-103">Tomar una instantánea y ver los procesos</span><span class="sxs-lookup"><span data-stu-id="6aab8-103">Taking a Snapshot and Viewing Processes</span></span>

<span data-ttu-id="6aab8-104">La siguiente aplicación de consola sencilla obtiene una lista de procesos en ejecución.</span><span class="sxs-lookup"><span data-stu-id="6aab8-104">The following simple console application obtains a list of running processes.</span></span> <span data-ttu-id="6aab8-105">En primer lugar, la `GetProcessList` función toma una instantánea de los procesos que se están ejecutando actualmente en el sistema mediante [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)y, a continuación, se recorre la lista registrada en la instantánea mediante [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) y [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next).</span><span class="sxs-lookup"><span data-stu-id="6aab8-105">First, the `GetProcessList` function takes a snapshot of currently executing processes in the system using [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot), and then it walks through the list recorded in the snapshot using [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next).</span></span> <span data-ttu-id="6aab8-106">Para cada proceso a su vez, `GetProcessList` llama a la `ListProcessModules` función que se describe en [recorrer la lista de módulos](traversing-the-module-list.md)y la `ListProcessThreads` función que se describe en [atravesar la lista de subprocesos](traversing-the-thread-list.md).</span><span class="sxs-lookup"><span data-stu-id="6aab8-106">For each process in turn, `GetProcessList` calls the `ListProcessModules` function which is described in [Traversing the Module List](traversing-the-module-list.md), and the `ListProcessThreads` function which is described in [Traversing the Thread List](traversing-the-thread-list.md).</span></span>

<span data-ttu-id="6aab8-107">Una función de generación de informes de errores simple, `printError` , muestra el motivo de los errores, que suelen ser el resultado de restricciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6aab8-107">A simple error-reporting function, `printError`, displays the reason for any failures, which usually result from security restrictions.</span></span> <span data-ttu-id="6aab8-108">Por ejemplo, se produce un error de [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) en los procesos inactivos y csrss porque sus restricciones de acceso impiden que el código de nivel de usuario los abra.</span><span class="sxs-lookup"><span data-stu-id="6aab8-108">For example, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span>


```C++
#include <windows.h>
#include <tlhelp32.h>
#include <tchar.h>

//  Forward declarations:
BOOL GetProcessList( );
BOOL ListProcessModules( DWORD dwPID );
BOOL ListProcessThreads( DWORD dwOwnerPID );
void printError( TCHAR* msg );

int main( void )
{
  GetProcessList( );
  return 0;
}

BOOL GetProcessList( )
{
  HANDLE hProcessSnap;
  HANDLE hProcess;
  PROCESSENTRY32 pe32;
  DWORD dwPriorityClass;

  // Take a snapshot of all processes in the system.
  hProcessSnap = CreateToolhelp32Snapshot( TH32CS_SNAPPROCESS, 0 );
  if( hProcessSnap == INVALID_HANDLE_VALUE )
  {
    printError( TEXT("CreateToolhelp32Snapshot (of processes)") );
    return( FALSE );
  }

  // Set the size of the structure before using it.
  pe32.dwSize = sizeof( PROCESSENTRY32 );

  // Retrieve information about the first process,
  // and exit if unsuccessful
  if( !Process32First( hProcessSnap, &pe32 ) )
  {
    printError( TEXT("Process32First") ); // show cause of failure
    CloseHandle( hProcessSnap );          // clean the snapshot object
    return( FALSE );
  }

  // Now walk the snapshot of processes, and
  // display information about each process in turn
  do
  {
    _tprintf( TEXT("\n\n=====================================================" ));
    _tprintf( TEXT("\nPROCESS NAME:  %s"), pe32.szExeFile );
    _tprintf( TEXT("\n-------------------------------------------------------" ));

    // Retrieve the priority class.
    dwPriorityClass = 0;
    hProcess = OpenProcess( PROCESS_ALL_ACCESS, FALSE, pe32.th32ProcessID );
    if( hProcess == NULL )
      printError( TEXT("OpenProcess") );
    else
    {
      dwPriorityClass = GetPriorityClass( hProcess );
      if( !dwPriorityClass )
        printError( TEXT("GetPriorityClass") );
      CloseHandle( hProcess );
    }

    _tprintf( TEXT("\n  Process ID        = 0x%08X"), pe32.th32ProcessID );
    _tprintf( TEXT("\n  Thread count      = %d"),   pe32.cntThreads );
    _tprintf( TEXT("\n  Parent process ID = 0x%08X"), pe32.th32ParentProcessID );
    _tprintf( TEXT("\n  Priority base     = %d"), pe32.pcPriClassBase );
    if( dwPriorityClass )
      _tprintf( TEXT("\n  Priority class    = %d"), dwPriorityClass );

    // List the modules and threads associated with this process
    ListProcessModules( pe32.th32ProcessID );
    ListProcessThreads( pe32.th32ProcessID );

  } while( Process32Next( hProcessSnap, &pe32 ) );

  CloseHandle( hProcessSnap );
  return( TRUE );
}


BOOL ListProcessModules( DWORD dwPID )
{
  HANDLE hModuleSnap = INVALID_HANDLE_VALUE;
  MODULEENTRY32 me32;

  // Take a snapshot of all modules in the specified process.
  hModuleSnap = CreateToolhelp32Snapshot( TH32CS_SNAPMODULE, dwPID );
  if( hModuleSnap == INVALID_HANDLE_VALUE )
  {
    printError( TEXT("CreateToolhelp32Snapshot (of modules)") );
    return( FALSE );
  }

  // Set the size of the structure before using it.
  me32.dwSize = sizeof( MODULEENTRY32 );

  // Retrieve information about the first module,
  // and exit if unsuccessful
  if( !Module32First( hModuleSnap, &me32 ) )
  {
    printError( TEXT("Module32First") );  // show cause of failure
    CloseHandle( hModuleSnap );           // clean the snapshot object
    return( FALSE );
  }

  // Now walk the module list of the process,
  // and display information about each module
  do
  {
    _tprintf( TEXT("\n\n     MODULE NAME:     %s"),   me32.szModule );
    _tprintf( TEXT("\n     Executable     = %s"),     me32.szExePath );
    _tprintf( TEXT("\n     Process ID     = 0x%08X"),         me32.th32ProcessID );
    _tprintf( TEXT("\n     Ref count (g)  = 0x%04X"),     me32.GlblcntUsage );
    _tprintf( TEXT("\n     Ref count (p)  = 0x%04X"),     me32.ProccntUsage );
    _tprintf( TEXT("\n     Base address   = 0x%08X"), (DWORD) me32.modBaseAddr );
    _tprintf( TEXT("\n     Base size      = %d"),             me32.modBaseSize );

  } while( Module32Next( hModuleSnap, &me32 ) );

  CloseHandle( hModuleSnap );
  return( TRUE );
}

BOOL ListProcessThreads( DWORD dwOwnerPID ) 
{ 
  HANDLE hThreadSnap = INVALID_HANDLE_VALUE; 
  THREADENTRY32 te32; 
 
  // Take a snapshot of all running threads  
  hThreadSnap = CreateToolhelp32Snapshot( TH32CS_SNAPTHREAD, 0 ); 
  if( hThreadSnap == INVALID_HANDLE_VALUE ) 
    return( FALSE ); 
 
  // Fill in the size of the structure before using it. 
  te32.dwSize = sizeof(THREADENTRY32); 
 
  // Retrieve information about the first thread,
  // and exit if unsuccessful
  if( !Thread32First( hThreadSnap, &te32 ) ) 
  {
    printError( TEXT("Thread32First") ); // show cause of failure
    CloseHandle( hThreadSnap );          // clean the snapshot object
    return( FALSE );
  }

  // Now walk the thread list of the system,
  // and display information about each thread
  // associated with the specified process
  do 
  { 
    if( te32.th32OwnerProcessID == dwOwnerPID )
    {
      _tprintf( TEXT("\n\n     THREAD ID      = 0x%08X"), te32.th32ThreadID ); 
      _tprintf( TEXT("\n     Base priority  = %d"), te32.tpBasePri ); 
      _tprintf( TEXT("\n     Delta priority = %d"), te32.tpDeltaPri ); 
      _tprintf( TEXT("\n"));
    }
  } while( Thread32Next(hThreadSnap, &te32 ) ); 

  CloseHandle( hThreadSnap );
  return( TRUE );
}

void printError( TCHAR* msg )
{
  DWORD eNum;
  TCHAR sysMsg[256];
  TCHAR* p;

  eNum = GetLastError( );
  FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS,
         NULL, eNum,
         MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
         sysMsg, 256, NULL );

  // Trim the end of the line and terminate it with a null
  p = sysMsg;
  while( ( *p > 31 ) || ( *p == 9 ) )
    ++p;
  do { *p-- = 0; } while( ( p >= sysMsg ) &&
                          ( ( *p == '.' ) || ( *p < 33 ) ) );

  // Display the message
  _tprintf( TEXT("\n  WARNING: %s failed with error %d (%s)"), msg, eNum, sysMsg );
}
```



## <a name="related-topics"></a><span data-ttu-id="6aab8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6aab8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aab8-110">Instantáneas del sistema</span><span class="sxs-lookup"><span data-stu-id="6aab8-110">Snapshots of the System</span></span>](snapshots-of-the-system.md)
</dt> </dl>

 

 