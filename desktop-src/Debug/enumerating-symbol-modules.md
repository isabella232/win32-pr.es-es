---
description: En el código siguiente se enumeran los módulos cargados por la función SymLoadModule64 o SymInitialize.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Enumerar módulos de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495797"
---
# <a name="enumerating-symbol-modules"></a>Enumerar módulos de símbolos

En el código siguiente se enumeran los módulos cargados por la función [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . La función [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) requiere una función de devolución de llamada, a la que se llamará una vez para cada módulo cargado. En este ejemplo, EnumModules (es una implementación de la función de devolución de llamada. En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



