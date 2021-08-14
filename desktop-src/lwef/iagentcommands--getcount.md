---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749831"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands::GetCount

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Recupera el número de objetos [**Command**](/windows/desktop/lwef/the-command-object) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Dirección de una variable que recibe el número de [**comandos de**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

*pdwCount incluye* solo el número de [**comandos que**](/windows/desktop/lwef/the-command-object) defina en la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) No se incluyen entradas de servidor u otras entradas de cliente.

 

 