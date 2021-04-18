---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704785"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Establece el juego de caracteres de la fuente que se muestra en el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Juego de caracteres de la fuente. A continuación se muestran algunos valores de configuración comunes para el valor:



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

El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. Puede cambiarlo con [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Sin embargo, el usuario puede invalidar el valor del juego de caracteres para todos los caracteres mediante la hoja de propiedades del agente de Microsoft. Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




