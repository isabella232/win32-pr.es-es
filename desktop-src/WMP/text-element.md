---
title: Elemento TEXT (Reproductor de Windows Media SDK)
description: Elemento TEXT
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Reproductor de Windows Media máscaras,elemento TEXT
- skins,TEXT, elemento
- Text, elemento
- referencia de máscaras,elemento TEXT
- elements,TEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c0d30393ef4fdeb62061ee58b0c7bd2f3f58bd685945e62c0e8062f22d881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122855"
---
# <a name="text-element"></a>Elemento TEXT

El **elemento TEXT** proporciona una manera de crear y controlar la apariencia del texto dentro de una máscara mediante los atributos siguientes. Los elementos **TEXT predefinidos** también se proporcionan para mayor comodidad.

El **elemento TEXT** admite los atributos siguientes.



| Atributo                                                   | Descripción                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](text-backgroundcolor.md)                 | Especifica o recupera el color de fondo del control Text.                                           |
| [cursor](text-cursor.md)                                   | Especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control Text.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Especifica o recupera el color de fondo utilizado para el control Text cuando está deshabilitado.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Especifica o recupera el estilo de fuente utilizado para el control Text cuando está deshabilitado.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Especifica o recupera el color de texto utilizado cuando el control Texto está deshabilitado.                               |
| [fontFace](text-fontface.md)                               | Especifica o recupera el tipo de letra del control Text.                                                   |
| [Fontsize](text-fontsize.md)                               | Especifica o recupera el tamaño de fuente del control Text.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.                                |
| [fontStyle](text-fontstyle.md)                             | Especifica o recupera el estilo de fuente para el control Text.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Especifica o recupera el color del texto para el control Text.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Especifica o recupera el color de fondo utilizado para el control Texto cuando el cursor del mouse se mantiene sobre él. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Especifica o recupera el estilo de fuente utilizado para el control Text cuando el cursor del mouse se mantiene sobre él.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Especifica o recupera el color de texto utilizado para el control Texto cuando el cursor del mouse se mantiene sobre él.       |
| [Justificación](text-justification.md)                     | Especifica o recupera la alineación del texto dentro del control Text.                                   |
| [Desplazamiento](text-scrolling.md)                             | Especifica o recupera un valor que indica si el texto se desplaza.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Especifica o recupera el número de píxeles que el texto se mueve durante cada movimiento de desplazamiento.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Especifica o recupera el retraso de tiempo entre los movimientos de desplazamiento.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Especifica o recupera la dirección del texto de desplazamiento.                                                 |
| [textWidth](text-textwidth.md)                             | Recupera el ancho en píxeles de la cadena contenida en el **atributo value.**                           |
| [Descripción](text-tooltip.md)                                 | Especifica o recupera el texto de información sobre herramientas para el control de texto.                                               |
| [value](text-value.md)                                     | Especifica o recupera el texto que se muestra en el control Texto.                                      |
| [Wordwrap](text-wordwrap.md)                               | Especifica o recupera un valor que indica si el ajuste de palabras está habilitado o deshabilitado.                     |



 

El **elemento TEXT** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente.](ambient-event-handlers.md)

Los elementos de texto predefinidos son elementos **TEXT** normales con varias configuraciones de atributo comunes especificadas de forma predeterminada. Están disponibles los siguientes elementos de texto predefinidos.



| TEXTO predefinido                                | Descripción                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Elemento **TEXT** con un agente de escucha integrado para **player.controls.currentPositionString.** |
| [DURATIONTEXT](durationtext.md)               | Elemento **TEXT** con un agente de escucha integrado para **player.currentMedia.DurationString.**    |
| [Statustext](statustext.md)                   | Elemento **TEXT con** un agente de escucha integrado para **player.status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Elemento **TEXT** con un agente de escucha integrado **para player.currentMedia.name**.              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




