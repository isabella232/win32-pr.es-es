---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075920"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon::GetBackColor

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera el valor para el color de fondo que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

Dirección de una variable que recibe la configuración de color para el fondo del globo.

</dd> </dl>

El color de fondo que se usa en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación. Sin embargo, el usuario puede cambiar el color de fondo de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




