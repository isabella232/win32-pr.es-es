---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74609f2e5f3201be07c425db17456f17e5202e6497b8b137815ae6124335650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976145"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet::GetPosition

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Recupera la posición de la ventana de hoja de propiedades de Microsoft Agent.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo de la hoja de propiedades en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde superior de la hoja de propiedades en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet::GetSize**](iagentpropertysheet--getsize.md)


 

 




