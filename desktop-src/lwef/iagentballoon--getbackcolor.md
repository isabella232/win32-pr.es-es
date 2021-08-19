---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888425"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon::GetBackColor

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera el valor del color de fondo que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

Dirección de una variable que recibe la configuración de color para el fondo del globo.

</dd> </dl>

El color de fondo utilizado en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarlo. Sin embargo, el usuario puede cambiar el color de fondo de los globos de palabras para todos los caracteres a través de la hoja de propiedades de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




