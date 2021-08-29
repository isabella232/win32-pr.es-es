---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabd35a43cba0485bbda1fae20b116316dec90832e42920d010b27586e972c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962335"
---
# <a name="iagentballoongetforecolor"></a>IAgentBalloon::GetForeColor

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Recupera el valor del color de primer plano que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*
</dt> <dd>

Dirección de una variable que recibe la configuración de color para el primer plano del globo.

</dd> </dl>

El color de primer plano utilizado en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarlo. Sin embargo, el usuario puede invalidar el color de primer plano de los globos de palabras para todos los caracteres a través de la hoja de propiedades de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md)


 

 




