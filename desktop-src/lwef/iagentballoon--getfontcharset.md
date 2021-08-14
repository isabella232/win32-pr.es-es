---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86237e96f2ec569926ec34e543dbdd187471ba21b49b38858b83853b61c55158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693357"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica el juego de caracteres de la fuente que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Dirección de un valor que recibe el juego de caracteres de la fuente. A continuación se muestra una configuración común para value:



| Valor    | Juego de caracteres                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caracteres Windows estándar (ANSI).                                                    |
| 1   | Juego de caracteres predeterminado.                                                                 |
| 2   | Juego de caracteres de símbolo.                                                              |
| 128 | Juego de caracteres de doble byte (DBCS) único para la versión japonesa de Windows.            |
| 129 | Juego de caracteres de doble byte (DBCS) único para la versión en coreano de Windows.              |
| 134 | Juego de caracteres de doble byte (DBCS) único para la versión en chino simplificado de Windows.  |
| 136 | Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows. |
| 255 | Normalmente, las aplicaciones MS-DOS muestran caracteres extendidos.                          |



 

</dd> </dl>

Para otros valores de juego de caracteres, consulte la documentación de Platform SDK.

El juego de caracteres predeterminado que se usa en el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent. Puede cambiarlo mediante [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md). Sin embargo, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres mediante la hoja de propiedades de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




