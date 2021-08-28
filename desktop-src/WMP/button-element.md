---
title: Elemento BUTTON (WMP)
description: Elemento BUTTON
ms.assetid: 2818ff6a-4fc5-4150-9ff9-ff143feb9204
keywords:
- Reproductor de Windows Media máscaras,elemento BUTTON
- máscaras, elemento BUTTON
- Button, elemento
- referencia de máscaras,elemento BUTTON
- elements,BUTTON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ca4e57dafdc01fc194c4cf4bc534e067297a58fcc2527939e3672f2d705628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736735"
---
# <a name="button-element"></a>Elemento BUTTON

El **elemento BUTTON** proporciona una manera de crear un botón dentro de una máscara. Los atributos siguientes se pueden usar para personalizar el comportamiento de un botón o se puede usar un botón predefinido para mayor comodidad.

El **elemento BUTTON** admite los atributos siguientes.



| Atributo                                         | Descripción                                                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](button-cursor.md)                       | Especifica o recupera el cursor que aparece cuando el puntero del mouse mantiene el puntero sobre **BUTTON**.                                                |
| [disabledImage](button-disabledimage.md)         | Especifica o recupera la imagen que se muestra cuando **button** está deshabilitado.                                                                  |
| [down](button-down.md)                           | Especifica o recupera un valor que indica si **button** está en la posición de arriba o abajo.                                                  |
| [downImage](button-downimage.md)                 | Especifica o recupera la imagen que representa el estado de apagado de **BUTTON.**                                                                  |
| [downToolTip](button-downtooltip.md)             | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre **button** y **button** está en estado de depresión o deprimido. |
| [hoverDownImage](button-hoverdownimage.md)       | Especifica o recupera la imagen que se muestra cuando **button** está en estado de bajada y el usuario mantiene el mouse sobre ella con el puntero del mouse.          |
| [hoverImage](button-hoverimage.md)               | Especifica o recupera la imagen que se muestra cuando **button** está en estado up y el usuario mantiene el mouse sobre ella con el puntero del mouse.            |
| [image](button-image.md)                         | Especifica o recupera la imagen predeterminada de **BUTTON.**                                                                                      |
| [Pegajoso](button-sticky.md)                       | Especifica o recupera un valor que indica si **BUTTON** es un botón de alternancia, es decir, si es un botón de dos estados o de un solo estado.         |
| [Baldosas](button-tiled.md)                         | Especifica o recupera un valor que indica si la **imagen BUTTON** se va a aplicar en mosaico.                                                            |
| [transparencyColor](button-transparencycolor.md) | Especifica o recupera el color que será transparente en la **imagen BUTTON.**                                                               |
| [upToolTip](button-uptooltip.md)                 | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre **button** y **button** está en estado up.                |



 

El **elemento BUTTON** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente.](ambient-event-handlers.md)

Los botones predefinidos son **elementos BUTTON** normales con varias configuraciones de atributo comunes especificadas de forma predeterminada. Están disponibles los siguientes botones predefinidos.



| BOTÓN predefinido                    | Descripción                                                                        |
|--------------------------------------|------------------------------------------------------------------------------------|
| [CLOSEBUTTON](closebutton.md)       | Botón **que** se usa para cerrar el reproductor.                                             |
| [FFWDBUTTON](ffwdbutton.md)         | Botón **con** una llamada integrada a **player.controls.fastForward** cuando se hace clic en él. |
| [Imagebutton](imagebutton.md)       | Botón **que** se usa para mostrar una imagen.                                             |
| [MINIMIZEBUTTON](minimizebutton.md) | Botón **que** se usa para minimizar el reproductor.                                          |
| [MUTEBUTTON](mutebutton.md)         | Botón **que** se usa para silenciar y desactivar el audio.                                   |
| [NEXTBUTTON](nextbutton.md)         | Botón **con** una llamada integrada a **player.controls.next cuando** se hace clic en él.        |
| [PAUSEBUTTON](pausebutton.md)       | Botón **con** una llamada integrada a **player.controls.pause cuando** se hace clic en él.       |
| [Playbutton](playbutton.md)         | Botón **con** una llamada integrada a **player.controls.play cuando** se hace clic en él.        |
| [PREVBUTTON](prevbutton.md)         | Botón **con** una llamada integrada a **player.controls.previous cuando** se hace clic en él.    |
| [REPEATBUTTON](repeatbutton.md)     | Botón **que** alterna la opción Repetir.                                       |
| [RETURNBUTTON](returnbutton.md)     | Botón **que** devuelve Reproductor de Windows Media al centro multimedia.                |
| [REWBUTTON](rewbutton.md)           | Botón **con** una llamada integrada a **player.controls.fastReverse cuando** se hace clic en él. |
| [SHUFFLEBUTTON](shufflebutton.md)   | Botón **que** alterna la opción Orden aleatorio.                                      |
| [STOPBUTTON](stopbutton.md)         | Botón **con** una llamada integrada a **player.controls.stop cuando** se hace clic en él.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




