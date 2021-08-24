---
description: En el código siguiente se muestra cómo llamar a la función SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recuperar información de símbolos por nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ec0a04ef2cac9dcd8256f8d00ff59b00bec449cdb4b5661566e7087e782cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076369"
---
# <a name="retrieving-symbol-information-by-name"></a>Recuperar información de símbolos por nombre

En el código siguiente se muestra cómo llamar a [**la función SymFromName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) Esta función rellena una estructura [**SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Dado que el nombre tiene una longitud variable, debe proporcionar un búfer lo suficientemente grande como para contener el nombre almacenado al final de la estructura **SYMBOL \_ INFO.** Además, el **miembro MaxNameLen** debe establecerse en el número de bytes reservados para el nombre. En este ejemplo, szSymbolName es un búfer que almacena el nombre del símbolo solicitado. En el ejemplo se supone que ha inicializado el controlador de símbolos mediante el código de [Inicializar el controlador de símbolos](initializing-the-symbol-handler.md).


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



Si una aplicación tiene un nombre de archivo de origen o módulo, así como información de número de línea, puede usar [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) para recuperar una dirección de código virtual. Esta función requiere un puntero a una [**estructura IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para recibir la dirección de código virtual. Tenga en cuenta que el controlador de símbolos solo puede recuperar información de número de línea cuando la opción SYMOPT LOAD LINES se establece \_ \_ mediante la función [**SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) Esta opción debe establecerse antes de cargar el módulo. El parámetro szModuleName contiene el nombre del módulo de origen; es opcional y puede ser **NULL.** El parámetro szFileName debe contener el nombre del archivo de origen y el parámetro dwLineNumber debe contener el número de línea para el que se recuperará la dirección virtual.


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



 

 



