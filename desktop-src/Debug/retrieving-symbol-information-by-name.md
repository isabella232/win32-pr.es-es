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
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="3f9e4-103">Recuperar información de símbolos por nombre</span><span class="sxs-lookup"><span data-stu-id="3f9e4-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="3f9e4-104">En el código siguiente se muestra cómo llamar a la función [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) .</span><span class="sxs-lookup"><span data-stu-id="3f9e4-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="3f9e4-105">Esta función rellena una estructura de [**\_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="3f9e4-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="3f9e4-106">Dado que el nombre tiene una longitud variable, debe proporcionar un búfer que sea lo suficientemente grande como para contener el nombre almacenado al final de la estructura de **\_ información de símbolos** .</span><span class="sxs-lookup"><span data-stu-id="3f9e4-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="3f9e4-107">Además, el miembro **MaxNameLen** debe establecerse en el número de bytes reservados para el nombre.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="3f9e4-108">En este ejemplo, szSymbolName es un búfer que almacena el nombre del símbolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="3f9e4-109">En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="3f9e4-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="3f9e4-110">Si una aplicación tiene un nombre de módulo o de archivo de origen, así como información de número de línea, puede usar [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) para recuperar una dirección de código virtual.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="3f9e4-111">Esta función requiere un puntero a una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para recibir la dirección del código virtual.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="3f9e4-112">Tenga en cuenta que el controlador de símbolos puede recuperar la información de números de línea solo cuando \_ \_ se establece la opción de carga de líneas de SYMOPT mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="3f9e4-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="3f9e4-113">Esta opción debe establecerse antes de cargar el módulo.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-113">This option must be set before loading the module.</span></span> <span data-ttu-id="3f9e4-114">El parámetro szModuleName contiene el nombre del módulo de origen; es opcional y puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="3f9e4-115">El parámetro szFileName debe contener el nombre del archivo de código fuente y el parámetro dwLineNumber debe contener el número de línea para el que se recuperará la dirección virtual.</span><span class="sxs-lookup"><span data-stu-id="3f9e4-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


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



 

 



