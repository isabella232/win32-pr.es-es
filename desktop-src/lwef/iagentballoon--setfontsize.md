---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6e19d79429ddf98f67a281cd11aefb1dc6bc2e54b1289e36c7cfb5a62bd538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976475"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Establece el tamaño de la fuente que se muestra en el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamaño de la fuente.

</dd> </dl>

El tamaño de fuente predeterminado utilizado en el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent. Puede cambiarlo con **IAgentBalloon::SetFontSize**. Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente para todos los caracteres mediante la hoja de propiedades de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetFontSize**](iagentballoon--getfontsize.md)


 

 




