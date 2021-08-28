---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725333"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Recupera el valor de la fuente mostrada en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Dirección de un BSTR que recibe el nombre de fuente que se muestra en un globo de palabras.

</dd> </dl>

La fuente predeterminada usada en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Puede cambiarlo con [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). El usuario puede invalidar la configuración de fuente de todos los caracteres mediante la hoja de propiedades de Microsoft Agent.

 

 




