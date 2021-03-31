---
title: Elemento BUTTON (WMP)
description: Elemento BUTTON
ms.assetid: 2818ff6a-4fc5-4150-9ff9-ff143feb9204
keywords:
- Aspectos de Windows Media Player, elemento BUTTON
- aspectos, elemento BUTTON
- Elemento BUTTON
- referencia de aspectos, elemento BUTTON
- elementos, botón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c069207e15be62e06b4d2b18f13c052026932dc
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2019
ms.locfileid: "103785141"
---
# <a name="button-element"></a>Elemento BUTTON

El elemento **Button** proporciona una manera de crear un botón dentro de una máscara. Los atributos siguientes se pueden usar para personalizar el comportamiento de un botón, o bien se puede usar un botón predefinido para mayor comodidad.

El elemento **Button** admite los siguientes atributos.



| Atributo                                         | Descripción                                                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](button-cursor.md)                       | Especifica o recupera el cursor que aparece cuando se mantiene el puntero del mouse sobre el **botón**.                                                |
| [disabledImage](button-disabledimage.md)         | Especifica o recupera la imagen que se muestra cuando el **botón** está deshabilitado.                                                                  |
| [vertical](button-down.md)                           | Especifica o recupera un valor que indica si el **botón** está en la posición arriba o abajo.                                                  |
| [downImage](button-downimage.md)                 | Especifica o recupera la imagen que representa el estado inactivo del **botón**.                                                                  |
| [downToolTip](button-downtooltip.md)             | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre el **botón** y el **botón** se encuentra en estado desactivado o presionado. |
| [hoverDownImage](button-hoverdownimage.md)       | Especifica o recupera la imagen que se muestra cuando el **botón** está en estado inactivo y el usuario mantiene el puntero del mouse sobre él.          |
| [hoverImage](button-hoverimage.md)               | Especifica o recupera la imagen que se muestra cuando el **botón** está en el estado up y el usuario mantiene el puntero del mouse sobre él.            |
| [image](button-image.md)                         | Especifica o recupera la imagen predeterminada del **botón**.                                                                                      |
| [rápidas](button-sticky.md)                       | Especifica o recupera un valor que indica si el **botón** es un control de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.         |
| [en mosaico](button-tiled.md)                         | Especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del **botón** .                                                            |
| [Property](button-transparencycolor.md) | Especifica o recupera el color que será transparente en la imagen del **botón** .                                                               |
| [Información sobre herramientas](button-uptooltip.md)                 | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre el **botón** y el **botón** está en estado activo.                |



 

El elemento **Button** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

Los botones predefinidos son elementos de **botón** normales con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes botones predefinidos.



| BOTÓN predefinido                    | Descripción                                                                        |
|--------------------------------------|------------------------------------------------------------------------------------|
| [CLOSEBUTTON](closebutton.md)       | Un **botón** que se usa para cerrar el reproductor.                                             |
| [FFWDBUTTON](ffwdbutton.md)         | Un **botón** con una llamada integrada a **Player. Controls. fastForward** cuando se hace clic en él. |
| [IMAGEBUTTON](imagebutton.md)       | Un **botón** que se usa para mostrar una imagen.                                             |
| [MINIMIZEBUTTON](minimizebutton.md) | Un **botón** que se usa para minimizar el reproductor.                                          |
| [MUTEBUTTON](mutebutton.md)         | Un **botón** que se usa para silenciar y dessilenciar el audio.                                   |
| [NEXTBUTTON](nextbutton.md)         | Un **botón** con una llamada integrada a **Player. Controls. Next** cuando se hace clic en él.        |
| [PAUSEBUTTON](pausebutton.md)       | Un **botón** con una llamada integrada a **Player. Controls. PAUSE** cuando se hace clic en él.       |
| [PLAYBUTTON](playbutton.md)         | Un **botón** con una llamada integrada a **Player. Controls. Play** cuando se hace clic en él.        |
| [PREVBUTTON](prevbutton.md)         | Un **botón** con una llamada integrada a **Player. Controls. Previous** cuando se hace clic en él.    |
| [REPEATBUTTON](repeatbutton.md)     | Un **botón** que alterna la opción de repetición.                                       |
| [RETURNBUTTON](returnbutton.md)     | Un **botón** que devuelve Windows Media Player a Media Center.                |
| [REWBUTTON](rewbutton.md)           | Un **botón** con una llamada integrada a **Player. Controls. fastReverse** cuando se hace clic en él. |
| [SHUFFLEBUTTON](shufflebutton.md)   | Un **botón** que alterna la opción de orden aleatorio.                                      |
| [STOPBUTTON](stopbutton.md)         | Un **botón** con una llamada integrada a **Player. Controls. Stop** cuando se hace clic en él.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




