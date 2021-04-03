---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075502"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter:: SetPosition

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Establece la posición del fotograma de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordenada de pantalla del borde izquierdo del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordenada de pantalla del borde superior del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> </dl>

La configuración de esta propiedad se aplica a todos los clientes del carácter. Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.

> [!Note]  
> A diferencia del método [**moveTo**](https://www.bing.com/search?q=**MoveTo**) , esta función no se pone en cola.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: GetPosition**](iagentcharacter--getposition.md)


 

 




