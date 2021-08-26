---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962495"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Recupera el valor del tamaño de la fuente que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Dirección de un valor que recibe el tamaño de la fuente.

</dd> </dl>

El tamaño de fuente predeterminado utilizado en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Puede cambiarlo con [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente de todos los caracteres mediante la hoja de propiedades de Microsoft Agent.

 

 




