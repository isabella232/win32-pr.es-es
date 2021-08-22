---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55abb64a8466b13ee41119e2a8a359ceeb182c92f7b4d2b1071547df07110052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750523"
---
# <a name="iagentcharacterexgetoriginalsize"></a>IAgentCharacterEx::GetOriginalSize

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera el tamaño original del marco de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Dirección de una variable que recibe el ancho original del marco de animación de caracteres en píxeles.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Dirección de una variable que recibe el alto original del marco de animación de caracteres en píxeles.

</dd> </dl>

Esta llamada devuelve el tamaño original del marco de caracteres tal y como se ha creado en el Editor de caracteres de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




