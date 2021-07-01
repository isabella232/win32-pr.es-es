---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120210"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Establece el juego de caracteres de la fuente que se muestra en el globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Juego de caracteres de la fuente. A continuación se muestra una configuración común para value:



| Valor    | Juego de caracteres                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caracteres estándar de Windows (ANSI).                                                    |
| 1   | Juego de caracteres predeterminado.                                                                 |
| 2   | Juego de caracteres de símbolo.                                                              |
| 128 | Juego de caracteres de doble byte (DBCS) único para la versión japonesa de Windows.            |
| 129 | Juego de caracteres de doble byte (DBCS) único para la versión en coreano de Windows.              |
| 134 | Juego de caracteres de doble byte (DBCS) único para la versión en chino simplificado de Windows.  |
| 136 | Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows. |
| 255 | Normalmente, las aplicaciones MS-DOS muestran caracteres extendidos.                          |



 

</dd> </dl>

Para otros valores de juego de caracteres, consulte la documentación del SDK de plataforma.

El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent. Puede cambiarlo con [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Sin embargo, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres mediante la hoja de propiedades de Microsoft Agent. Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




