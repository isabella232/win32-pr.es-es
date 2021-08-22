---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63e75111b7694fcb993e141b8534e8f174efd1a1a252f250167ecb597149f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609995"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter::GetPosition

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Recupera la posición del fotograma de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo del marco de animación de caracteres en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Dirección de una variable que recibe la coordenada de pantalla del borde superior del marco de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en su marco de animación rectangular.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




