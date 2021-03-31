---
description: En el código siguiente se muestra cómo llamar a la función SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recuperar información de símbolos por nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152972"
---
# <a name="retrieving-symbol-information-by-name"></a>Recuperar información de símbolos por nombre

En el código siguiente se muestra cómo llamar a la función [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Esta función rellena una estructura de [**\_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Dado que el nombre tiene una longitud variable, debe proporcionar un búfer que sea lo suficientemente grande como para contener el nombre almacenado al final de la estructura de **\_ información de símbolos** . Además, el miembro **MaxNameLen** debe establecerse en el número de bytes reservados para el nombre. En este ejemplo, szSymbolName es un búfer que almacena el nombre del símbolo solicitado. En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



Si una aplicación tiene un nombre de módulo o de archivo de origen, así como información de número de línea, puede usar [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) para recuperar una dirección de código virtual. Esta función requiere un puntero a una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para recibir la dirección del código virtual. Tenga en cuenta que el controlador de símbolos puede recuperar la información de números de línea solo cuando \_ \_ se establece la opción de carga de líneas de SYMOPT mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Esta opción debe establecerse antes de cargar el módulo. El parámetro szModuleName contiene el nombre del módulo de origen; es opcional y puede ser **null**. El parámetro szFileName debe contener el nombre del archivo de código fuente y el parámetro dwLineNumber debe contener el número de línea para el que se recuperará la dirección virtual.


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



