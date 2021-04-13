---
title: Elemento TEXT (SDK de Windows Media Player)
description: Elemento TEXT
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Aspectos de Windows Media Player, elemento de texto
- aspectos, elemento de texto
- Elemento TEXT
- referencia de las máscaras, elemento de texto
- elementos, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acdad737fda44cc0e090eb13fb20c765b447ccbd
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104358460"
---
# <a name="text-element"></a>Elemento TEXT

El elemento de **texto** proporciona una manera de crear y controlar el aspecto del texto dentro de una máscara mediante el uso de los siguientes atributos. También se proporcionan elementos de **texto** predefinidos para mayor comodidad.

El elemento de **texto** admite los siguientes atributos.



| Atributo                                                   | Descripción                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](text-backgroundcolor.md)                 | Especifica o recupera el color de fondo del control de texto.                                           |
| [cursor](text-cursor.md)                                   | Especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control de texto.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Especifica o recupera el color de fondo usado para el control de texto cuando está deshabilitado.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Especifica o recupera el estilo de fuente utilizado para el control de texto cuando está deshabilitado.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Especifica o recupera el color de texto utilizado cuando se deshabilita el control de texto.                               |
| [fontFace](text-fontface.md)                               | Especifica o recupera el tipo de letra para el control de texto.                                                   |
| [fontSize](text-fontsize.md)                               | Especifica o recupera el tamaño de fuente para el control de texto.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.                                |
| [fontStyle](text-fontstyle.md)                             | Especifica o recupera el estilo de fuente para el control de texto.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Especifica o recupera el color del texto del control de texto.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Especifica o recupera el color de fondo usado para el control de texto cuando el cursor del mouse se desplaza sobre él. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Especifica o recupera el estilo de fuente utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Especifica o recupera el color de texto utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.       |
| [motivación](text-justification.md)                     | Especifica o recupera la alineación del texto en el control de texto.                                   |
| [desplazamiento](text-scrolling.md)                             | Especifica o recupera un valor que indica si el texto se desplaza.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Especifica o recupera el número de píxeles que se mueve el texto durante cada movimiento de desplazamiento.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Especifica o recupera el tiempo de retardo entre los movimientos de desplazamiento.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Especifica o recupera la dirección del texto de desplazamiento.                                                 |
| [textWidth](text-textwidth.md)                             | Recupera el ancho en píxeles de la cadena incluida en el atributo de **valor** .                           |
| [Herramienta](text-tooltip.md)                                 | Especifica o recupera el texto de información sobre herramientas para el control de texto.                                               |
| [value](text-value.md)                                     | Especifica o recupera el texto que se muestra en el control de texto.                                      |
| [Ajuste](text-wordwrap.md)                               | Especifica o recupera un valor que indica si está habilitado o deshabilitado el ajuste de palabras.                     |



 

El elemento de **texto** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

Los elementos de texto predefinidos son elementos de **texto** normal con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes elementos de texto predefinidos.



| TEXTO predefinido                                | Descripción                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Un elemento de **texto** con un agente de escucha integrado para **Player. Controls. currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Un elemento de **texto** con un agente de escucha integrado para **Player. currentMedia. DurationString**.    |
| [STATUSTEXT](statustext.md)                   | Un elemento de **texto** con un agente de escucha integrado para **Player. status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Un elemento de **texto** con un agente de escucha integrado para **Player.currentMedia.Name**.              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




