---
title: Elemento SLIDEr
description: Elemento SLIDEr
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Aspectos de Windows Media Player, elemento SLIDEr
- Skins, elemento SLIDEr
- Elemento SLIDEr
- referencia de las máscaras, elemento SLIDEr
- elementos, control deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357238"
---
# <a name="slider-element"></a>Elemento SLIDEr

El elemento **Slider** proporciona una manera de crear y manipular un control deslizante horizontal o vertical simple. Admite los siguientes atributos y controladores de eventos. También se proporcionan elementos de **control deslizante** predefinidos para mayor comodidad.

El elemento **Slider** admite los siguientes atributos.



| Atributo                                                 | Descripción                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](slider-backgroundcolor.md)             | Especifica o recupera el color de fondo del control deslizante.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Especifica o recupera el color final del fondo del control deslizante.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Especifica o recupera la imagen de fondo del control deslizante que aparece al mantener el mouse sobre él.      |
| [backgroundImage](slider-backgroundimage.md)             | Especifica o recupera la imagen de fondo predeterminada del control deslizante.                                                |
| [Border](slider-bordersize.md)                       | Especifica o recupera el tamaño del borde en píxeles.                                                                 |
| [cursor](slider-cursor.md)                               | Especifica o recupera un valor que indica qué tipo de cursor aparece cuando el mouse está encima del control deslizante. |
| [direction](slider-direction.md)                         | Especifica o recupera la dirección en la que se colocan las imágenes de control deslizante.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Especifica o recupera el color deshabilitado del control deslizante.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Especifica o recupera la imagen del control deslizante que aparece cuando el control está deshabilitado.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Especifica o recupera el color de primer plano del control deslizante.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Especifica o recupera el color final del primer plano del control deslizante.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Especifica o recupera la imagen de primer plano del control deslizante que aparece al mantener el mouse sobre él.      |
| [foregroundImage](slider-foregroundimage.md)             | Especifica o recupera la imagen de primer plano predeterminada del control deslizante.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Especifica o recupera la posición actual de la barra de progreso de primer plano como un porcentaje del área del control deslizante.    |
| [max](slider-max.md)                                     | Especifica o recupera el valor máximo del intervalo definido por el control deslizante.                              |
| [min](slider-min.md)                                     | Especifica o recupera el valor mínimo del intervalo definido por el control deslizante.                              |
| [controles](slider-slide.md)                                 | Especifica o recupera un valor que indica si la imagen de primer plano se desplaza sobre la imagen de fondo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Especifica o recupera la imagen de Thumb deshabilitada del control deslizante.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Especifica o recupera la imagen que representa el estado inactivo del control de posición.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Especifica o recupera la imagen del control de posición que aparece al mantener el mouse sobre él.                  |
| [thumbImage](slider-thumbimage.md)                       | Especifica o recupera la imagen que se utilizará para representar la posición actual del control deslizante.               |
| [en mosaico](slider-tiled.md)                                 | Especifica o recupera un valor que indica si las imágenes del control deslizante se van a colocar en mosaico.                                |
| [Herramienta](slider-tooltip.md)                             | Especifica o recupera el texto de información sobre herramientas para el control deslizante.                                                   |
| [Property](slider-transparencycolor.md)         | Especifica o recupera el color transparente de las imágenes del control deslizante.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Especifica o recupera un valor que indica si se utilizará la barra de progreso en primer plano.                       |
| [value](slider-value.md)                                 | Especifica y recupera la posición actual del control deslizante.                                                       |



 

El elemento **Slider** puede implementar los controladores de eventos siguientes.



| Controlador de eventos                                   | Descripción                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Controla un evento que se produce cuando el usuario hace clic y mantiene presionado el botón primario del mouse y comienza a arrastrar el mouse. |
| [onDragEnd](slider-ondragend.md)               | Controla un evento que se produce cuando se suelta el botón primario del mouse después de una operación de arrastre.                      |
| [onPositionChange](slider-onpositionchange.md) | Controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra.   |



 

El elemento **Slider** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

Los controles deslizantes predefinidos son elementos de **control deslizante** normales con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes controles deslizantes predefinidos.



| Control deslizante predefinido                  | Descripción                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | **Control deslizante** que se usa para establecer el equilibrio de audio.                        |
| [SEEKSLIDER](seekslider.md)       | **Control deslizante** que se usa para buscar cualquier posición dentro de un archivo multimedia. |
| [VOLUMESLIDER](volumeslider.md)   | **Control deslizante** que se usa para establecer el volumen de audio.                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




