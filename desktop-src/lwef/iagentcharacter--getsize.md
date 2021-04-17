---
title: IAgentCharacter se obtiene
description: IAgentCharacter se obtiene
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357792"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter:: obtiene

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera el tamaño del fotograma de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Dirección de una variable que recibe el ancho del fotograma de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Dirección de una variable que recibe el alto del fotograma de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: setSize**](iagentcharacter--setsize.md)


 

 




