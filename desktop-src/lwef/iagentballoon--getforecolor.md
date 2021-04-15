---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714243"
---
# <a name="iagentballoongetforecolor"></a>IAgentBalloon::GetForeColor

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Recupera el valor del color de primer plano mostrado en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*
</dt> <dd>

Dirección de una variable que recibe la configuración de color para el globo de primer plano.

</dd> </dl>

El color de primer plano utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación. Sin embargo, el usuario puede invalidar el color de primer plano de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md)


 

 




