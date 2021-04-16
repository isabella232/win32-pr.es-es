---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269416"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Recupera el valor para el tamaño de la fuente que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Dirección de un valor que recibe el tamaño de la fuente.

</dd> </dl>

El tamaño de fuente predeterminado utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft. Puede cambiarlo con [**IAgentBalloon:: SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.

 

 




