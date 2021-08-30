---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc48eeba39a889c5a7cbee9bc9caeef759571e98b904646c62cd903c444305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962615"
---
# <a name="iagentballoongetfontbold"></a>IAgentBalloon::GetFontBold

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Indica si la fuente usada en un globo de palabras está en negrita.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*
</dt> <dd>

Dirección de un valor que recibe **True si** la fuente está en negrita y **False** si no está en negrita.

</dd> </dl>

El estilo de fuente utilizado en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarlo. Sin embargo, el usuario puede invalidar la configuración de fuente de todos los caracteres a través de la hoja de propiedades de Microsoft Agent.

 

 




