---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357793"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter:: GetPosition

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Recupera la posición del marco de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde superior del fotograma de la animación de caracteres en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> </dl>

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter:: se obtiene**](iagentcharacter--getsize.md)


 

 




