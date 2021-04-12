---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357665"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Establece el tamaño de la fuente que se muestra en el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamaño de la fuente.

</dd> </dl>

El tamaño de fuente predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. Puede cambiarlo con **IAgentBalloon:: SetFontSize**. Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetFontSize**](iagentballoon--getfontsize.md)


 

 




