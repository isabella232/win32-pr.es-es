---
description: En el código siguiente se muestra cómo recuperar un nombre de símbolo no decorado de un nombre de símbolo mediante UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recuperar nombres de símbolos no decorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076349"
---
# <a name="retrieving-undecorated-symbol-names"></a>Recuperar nombres de símbolos no decorados

En el código siguiente se muestra cómo recuperar un nombre de símbolo no decorado de un nombre de símbolo [**mediante UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname). El nombre decorado se almacena en `szName` . En el ejemplo se supone que ha inicializado el controlador de símbolos mediante el código de [Inicializar el controlador de símbolos](initializing-the-symbol-handler.md).


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



 

 



