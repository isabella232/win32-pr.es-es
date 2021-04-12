---
title: Tamaño de IAgentNotifySink
description: Tamaño de IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532290"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink:: Size

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Notifica a una aplicación cliente cuando se ha cambiado el tamaño del carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter cuyo tamaño se ha cambiado.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Ancho del fotograma de animación del carácter en píxeles.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Alto del fotograma de animación del carácter en píxeles.

</dd> </dl>

Este evento se envía a todos los clientes del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::**](iagentcharacter--getsize.md), [ **IAgentCharacter:: setSize**](iagentcharacter--setsize.md)


 

 




