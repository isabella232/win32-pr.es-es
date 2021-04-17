---
title: IAgentPropertySheet se obtiene
description: IAgentPropertySheet se obtiene
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704668"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet:: obtiene

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Recupera el tamaño de la ventana de la hoja de propiedades del agente de Microsoft.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Dirección de una variable que recibe el ancho de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Dirección de una variable que recibe el alto de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentPropertySheet:: GetPosition**](iagentpropertysheet--getposition.md)


 

 




