---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420537"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands:: GetCount

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Recupera el número de objetos de [**comando**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Dirección de una variable que recibe el número de [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

*pdwCount* incluye solo el número de [**comandos**](/windows/desktop/lwef/the-command-object) que se definen en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . No se incluyen las entradas de servidor o de otro cliente.

 

 