---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962235"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter::GetSize

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera el tamaño del marco de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Dirección de una variable que recibe el ancho del marco de animación de caracteres en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Dirección de una variable que recibe el alto del marco de animación de caracteres en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en su marco de animación rectangular.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)


 

 




