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
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="842e7-103">Recuperar información de símbolos por dirección</span><span class="sxs-lookup"><span data-stu-id="842e7-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="842e7-104">En el código siguiente se muestra cómo llamar a la función [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) .</span><span class="sxs-lookup"><span data-stu-id="842e7-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="842e7-105">Esta función rellena una estructura de [**\_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="842e7-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="842e7-106">Dado que el nombre tiene una longitud variable, debe proporcionar un búfer que sea lo suficientemente grande como para contener el nombre almacenado al final de la estructura de **\_ información de símbolos** .</span><span class="sxs-lookup"><span data-stu-id="842e7-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="842e7-107">Además, el miembro **MaxNameLen** debe establecerse en el número de bytes reservados para el nombre.</span><span class="sxs-lookup"><span data-stu-id="842e7-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="842e7-108">En este ejemplo, *dwAddress* es la dirección que se asignará a un símbolo.</span><span class="sxs-lookup"><span data-stu-id="842e7-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="842e7-109">La función **SymFromAddr** almacenará un desplazamiento al principio del símbolo en la dirección de *dwDisplacement*.</span><span class="sxs-lookup"><span data-stu-id="842e7-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="842e7-110">En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="842e7-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="842e7-111">Para recuperar el número de línea del código fuente de una dirección especificada, una aplicación puede utilizar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span><span class="sxs-lookup"><span data-stu-id="842e7-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="842e7-112">Esta función requiere un puntero a una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para recibir el nombre del archivo de código fuente y el número de línea correspondiente a una dirección de código especificada.</span><span class="sxs-lookup"><span data-stu-id="842e7-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="842e7-113">Tenga en cuenta que el controlador de símbolos puede recuperar la información de números de línea solo cuando se establece **SYMOPT para \_ cargar \_ líneas** mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="842e7-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="842e7-114">Esta opción debe establecerse antes de cargar el módulo.</span><span class="sxs-lookup"><span data-stu-id="842e7-114">This option must be set before loading the module.</span></span> <span data-ttu-id="842e7-115">El parámetro dwAddress contiene la dirección de código para la que se ubicará el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="842e7-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


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



 

 



