---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268948"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica el juego de caracteres de la fuente que se muestra en un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Dirección de un valor que recibe el juego de caracteres de la fuente. A continuación se muestran algunos valores de configuración comunes para el valor:



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caracteres estándar de Windows (ANSI).                                                    |
| 1   | Juego de caracteres predeterminado.                                                                 |
| 2   | Juego de caracteres de símbolos.                                                              |
| 128 | Juego de caracteres de doble byte (DBCS) único para la versión en japonés de Windows.            |
| 129 | Juego de caracteres de doble byte (DBCS) único para la versión coreana de Windows.              |
| 134 | Juego de caracteres de doble byte (DBCS) único para la versión de chino simplificado de Windows.  |
| 136 | Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows. |
| 255 | Caracteres extendidos que suelen mostrar las aplicaciones de MS-DOS.                          |



 

</dd> </dl>

Para otros valores de juego de caracteres, consulte la documentación del SDK de la plataforma.

El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. Puede cambiarlo mediante [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md). Sin embargo, el usuario puede invalidar el valor del juego de caracteres para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




