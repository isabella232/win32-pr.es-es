---
title: SUBVIEW( Elemento)
description: SUBVIEW( Elemento)
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Reproductor de Windows Media máscaras, elemento SUBVIEW
- skins,SUBVIEW, elemento
- SUBVIEW, elemento
- referencia de máscaras, elemento SUBVIEW
- elements,SUBVIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef4f7860d1db04991a35ffeff2903e7a16a5d7bd84929313c296006f6f1c092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122915"
---
# <a name="subview-element"></a>SUBVIEW( Elemento)

El **elemento SUBVIEW** proporciona una manera de manipular una parte de una máscara, por ejemplo, para proporcionar un panel de control que se puede ocultar cuando no se está utilizando. **Los elementos SUBVIEW** siempre son elementos secundarios de elementos **VIEW** primarios y pueden contener otros elementos de máscara, excepto **VIEW**, **THEME** y otros **elementos SUBVIEW.**

El **elemento SUBVIEW** admite los siguientes atributos, que se definen en el **elemento VIEW.**



| Atributo                                                       | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](view-backgroundcolor.md)                     | Especifica o recupera el color de fondo del control **SUBVIEW.** El valor predeterminado es "none".        |
| [backgroundImage](view-backgroundimage.md)                     | Especifica o recupera la imagen de fondo del control **SUBVIEW.**                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica o recupera el valor de saturación de la imagen de fondo.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Especifica o recupera un valor que indica si la imagen de fondo del control **SUBVIEW** está en mosaico. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.                      |
| [transparencyColor](view-transparencycolor.md)                 | Especifica o recupera el color de transparencia de la imagen de fondo.                                      |



 

El **elemento SUBVIEW** admite los atributos de ambiente, excepto donde se indica. Para obtener más información, vea [Atributos ambientales.](ambient-attributes.md)

El **elemento SUBVIEW** puede implementar los siguientes controladores de eventos de ambiente: [onendmove](onendmove.md) [y onresize](onresize.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 




