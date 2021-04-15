---
title: IAgentCommandWindow se obtiene
description: IAgentCommandWindow se obtiene
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714193"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow:: obtiene

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Recupera el tamaño actual de la ventana comandos de voz.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Dirección de una variable que recibe el ancho de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Dirección de una variable que recibe el alto de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommandWindow:: GetPosition**](iagentcommandwindow--getposition.md)


 

 




