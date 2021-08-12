---
title: Elemento SLIDER
description: Elemento SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Reproductor de Windows Media máscaras, elemento SLIDER
- máscaras, elemento SLIDER
- Elemento SLIDER
- referencia de máscaras,elemento SLIDER
- elements,SLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140c84f6bec826b34ff4e1c5a4a3365d44ba9aa67ca9504cea642aba25f076d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569097"
---
# <a name="slider-element"></a>Elemento SLIDER

El **elemento SLIDER** proporciona una manera de crear y manipular un control deslizante horizontal o vertical simple. Admite los siguientes atributos y controladores de eventos. Los elementos **SLIDER** predefinidos también se proporcionan para mayor comodidad.

El **elemento SLIDER** admite los atributos siguientes.



| Atributo                                                 | Descripción                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](slider-backgroundcolor.md)             | Especifica o recupera el color de fondo del control deslizante.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Especifica o recupera el color final de fondo del control deslizante.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Especifica o recupera la imagen de fondo del control deslizante que aparece al mantener el puntero sobre él con el mouse.      |
| [backgroundImage](slider-backgroundimage.md)             | Especifica o recupera la imagen de fondo predeterminada del control deslizante.                                                |
| [borderSize](slider-bordersize.md)                       | Especifica o recupera el tamaño del borde en píxeles.                                                                 |
| [cursor](slider-cursor.md)                               | Especifica o recupera un valor que indica qué tipo de cursor aparece cuando el mouse está sobre el control deslizante. |
| [direction](slider-direction.md)                         | Especifica o recupera la dirección en la que se menten las imágenes de control deslizante.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Especifica o recupera el color deshabilitado del control deslizante.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Especifica o recupera la imagen del control deslizante que aparece cuando el control está deshabilitado.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Especifica o recupera el color de primer plano del control deslizante.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Especifica o recupera el color final de primer plano del control deslizante.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Especifica o recupera la imagen de primer plano del control deslizante que aparece al mantener el puntero sobre él con el mouse.      |
| [foregroundImage](slider-foregroundimage.md)             | Especifica o recupera la imagen de primer plano predeterminada del control deslizante.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Especifica o recupera la posición actual de la barra de progreso de primer plano como porcentaje del área deslizante.    |
| [max](slider-max.md)                                     | Especifica o recupera el valor máximo del intervalo definido por el control deslizante.                              |
| [min](slider-min.md)                                     | Especifica o recupera el valor mínimo del intervalo definido por el control deslizante.                              |
| [Deslice](slider-slide.md)                                 | Especifica o recupera un valor que indica si la imagen de primer plano se desliza sobre la imagen de fondo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Especifica o recupera la imagen de posición deshabilitada del control deslizante.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Especifica o recupera la imagen que representa el estado de bajada del control.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Especifica o recupera la imagen del control que aparece al mantener el puntero sobre ella con el mouse.                  |
| [thumbImage](slider-thumbimage.md)                       | Especifica o recupera la imagen que se usará para representar la posición actual del control deslizante.               |
| [Baldosas](slider-tiled.md)                                 | Especifica o recupera un valor que indica si las imágenes del control deslizante se van a en mosaico.                                |
| [Descripción](slider-tooltip.md)                             | Especifica o recupera el texto de información sobre herramientas para el control deslizante.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Especifica o recupera el color transparente de las imágenes del control deslizante.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Especifica o recupera un valor que indica si se usará la barra de progreso de primer plano.                       |
| [value](slider-value.md)                                 | Especifica y recupera la posición actual del control deslizante.                                                       |



 

El **elemento SLIDER** puede implementar los siguientes controladores de eventos.



| Controlador de eventos                                   | Descripción                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Controla un evento que tiene lugar cuando el usuario hace clic y mantiene presionado el botón izquierdo del mouse y comienza a arrastrar el mouse. |
| [onDragEnd](slider-ondragend.md)               | Controla un evento que tiene lugar cuando se libera el botón izquierdo del mouse después de una operación de arrastre.                      |
| [onPositionChange](slider-onpositionchange.md) | Controla un evento que tiene lugar cuando cambia la posición del control deslizante como resultado de que el usuario hace clic o arrastra.   |



 

El **elemento SLIDER** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente.](ambient-event-handlers.md)

Los controles deslizantes predefinidos son **elementos SLIDER** normales con varios valores de atributo comunes especificados de forma predeterminada. Están disponibles los siguientes controles deslizantes predefinidos.



| CONTROL DESLIZANTE predefinido                  | Descripción                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | Control **SLIDER que** se usa para establecer el equilibrio de audio.                        |
| [SEEKSLIDER](seekslider.md)       | Control **SLIDER** que se usa para buscar cualquier posición dentro de un archivo multimedia. |
| [VOLUMESLIDER](volumeslider.md)   | Control **SLIDER que** se usa para establecer el volumen de audio.                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




