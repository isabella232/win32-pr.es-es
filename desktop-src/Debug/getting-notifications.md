---
description: En el código siguiente se muestra cómo obtener y notificar información de estado detallada del controlador de símbolos sobre la búsqueda y carga de módulos y los archivos de símbolos correspondientes.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Obtener notificaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275094"
---
# <a name="getting-notifications"></a>Obtener notificaciones

En el código siguiente se muestra cómo obtener y notificar información de estado detallada del controlador de símbolos sobre la búsqueda y carga de módulos y los archivos de símbolos correspondientes.

Muchos familiarizados con el depurador de WinDbg pueden recordar un comando llamado "! SYM ruidoso". Este comando lo usa el usuario para determinar por qué WinDbg es o no puede cargar archivos de símbolos. Muestra una lista detallada de todo lo que el controlador de símbolos intenta.

Esta misma lista también está disponible para cualquier persona que desarrolle un cliente al controlador de símbolos de DbgHelp.

En primer lugar, llame a [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ Debug**. Esto hace que DbgHelp Active las notificaciones de depuración.

Después de llamar a [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) para registrar una función de devolución de llamada a la que se llamará DbgHelp cada vez que se produzca un evento interesante. En este ejemplo, la función de devolución de llamada se denomina [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback). A las funciones de devolución de llamada de símbolos se les pasa una variedad de códigos de acción que pueden controlar según el tipo. En este ejemplo, solo se controla el código de la acción de **\_ evento CBA** . Esta función pasa una cadena que contiene información detallada sobre un evento que se produjo en el proceso de carga de un símbolo. Este evento puede ser cualquier cosa desde un intento de leer los datos de una imagen ejecutable hasta la ubicación correcta de un archivo de símbolos. **SymRegisterCallbackProc64** muestra esa cadena y devuelve **true**.

> [!IMPORTANT]
> Asegúrese de que devuelve **false** a cada código de acción que no controla; de lo contrario, puede experimentar un comportamiento indefinido. Consulte [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) para obtener una lista de todos los códigos de acción y sus implicaciones.

 

Ahora que la devolución de llamada está registrada, es el momento de cargar el módulo especificado en la línea de comandos mediante una llamada a [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).

Por último, llame a [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) antes de salir.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



Si se especifica **null** como el segundo parámetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , se indica que el controlador de símbolos debe usar la ruta de búsqueda predeterminada para buscar archivos de símbolos. Para obtener información detallada sobre cómo el controlador de símbolos busca archivos de símbolos o cómo una aplicación puede especificar una ruta de búsqueda de símbolos, vea rutas de acceso de [símbolos](symbol-paths.md).

La ejecución de este programa muestra cómo se procesa la ruta de acceso de símbolos. Como DbgHelp busca el archivo de símbolos a través de la ruta de acceso de símbolos, llama repetidamente a [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) que, a su vez, muestra las siguientes cadenas que se pasan por DbgHelp.

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



