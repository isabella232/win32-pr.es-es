---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704669"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet:: GetPosition

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Recupera la posición de la ventana de la hoja de propiedades del agente de Microsoft.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde superior de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet:: obtiene**](iagentpropertysheet--getsize.md)


 

 




