---
description: En el código siguiente se muestra cómo llamar a la función SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Recuperar información de símbolos por dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152973"
---
# <a name="retrieving-symbol-information-by-address"></a>Recuperar información de símbolos por dirección

En el código siguiente se muestra cómo llamar a la función [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Esta función rellena una estructura de [**\_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Dado que el nombre tiene una longitud variable, debe proporcionar un búfer que sea lo suficientemente grande como para contener el nombre almacenado al final de la estructura de **\_ información de símbolos** . Además, el miembro **MaxNameLen** debe establecerse en el número de bytes reservados para el nombre. En este ejemplo, *dwAddress* es la dirección que se asignará a un símbolo. La función **SymFromAddr** almacenará un desplazamiento al principio del símbolo en la dirección de *dwDisplacement*. En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



Para recuperar el número de línea del código fuente de una dirección especificada, una aplicación puede utilizar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr). Esta función requiere un puntero a una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para recibir el nombre del archivo de código fuente y el número de línea correspondiente a una dirección de código especificada. Tenga en cuenta que el controlador de símbolos puede recuperar la información de números de línea solo cuando se establece **SYMOPT para \_ cargar \_ líneas** mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Esta opción debe establecerse antes de cargar el módulo. El parámetro dwAddress contiene la dirección de código para la que se ubicará el nombre del archivo de código fuente y el número de línea.


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



