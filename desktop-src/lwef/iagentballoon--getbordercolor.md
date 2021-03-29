---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777581"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon::GetBorderColor

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Recupera el valor del color del borde que se muestra para un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*
</dt> <dd>

Dirección de una variable que recibe la configuración de color para el borde del globo.

</dd> </dl>

El color del borde de un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación. Sin embargo, el usuario puede cambiar el color del borde de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon:: getBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)


 

 




