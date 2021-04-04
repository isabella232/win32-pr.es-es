---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076307"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon::SetFontName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Establece la fuente que se muestra en el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR que establece la fuente mostrada en el globo de palabras.

</dd> </dl>

La fuente predeterminada utilizada en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. Puede cambiarlo con **IAgentBalloon:: SetFontName**. Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon:: GetVisible**](iagentballoon--getvisible.md)


 

 




