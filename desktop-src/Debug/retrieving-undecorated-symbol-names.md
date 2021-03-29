---
description: En el código siguiente se muestra cómo recuperar un nombre de símbolo no representativo de un nombre de símbolo mediante UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recuperar nombres de símbolos no representativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648171"
---
# <a name="retrieving-undecorated-symbol-names"></a><span data-ttu-id="c9628-103">Recuperar nombres de símbolos no representativos</span><span class="sxs-lookup"><span data-stu-id="c9628-103">Retrieving Undecorated Symbol Names</span></span>

<span data-ttu-id="c9628-104">En el código siguiente se muestra cómo recuperar un nombre de símbolo no representativo de un nombre de símbolo mediante [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span><span class="sxs-lookup"><span data-stu-id="c9628-104">The following code demonstrates how to retrieve an undecorated symbol name from a symbol name using [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span></span> <span data-ttu-id="c9628-105">El nombre representativo se almacena en `szName` .</span><span class="sxs-lookup"><span data-stu-id="c9628-105">The decorated name is stored in `szName`.</span></span> <span data-ttu-id="c9628-106">En el ejemplo se da por supuesto que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="c9628-106">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



