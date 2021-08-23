---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665645"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter::SetPosition

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Establece la posición del marco de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordenada de pantalla del borde izquierdo del marco de animación de caracteres en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordenada de pantalla del borde superior del marco de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

La configuración de esta propiedad se aplica a todos los clientes del carácter. Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en su marco de animación rectangular.

> [!Note]  
> A diferencia [**del método MoveTo,**](https://www.bing.com/search?q=**MoveTo**) esta función no se pone en cola.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetPosition**](iagentcharacter--getposition.md)


 

 




