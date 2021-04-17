---
title: SLIDEr. foregroundImage
description: El atributo foregroundImage especifica o recupera la imagen de primer plano del control deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- CONTROL SLIDEr. foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661191"
---
# <a name="sliderforegroundimage"></a>SLIDEr. foregroundImage

El atributo **foregroundImage** especifica o recupera la imagen de primer plano del control deslizante.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Al usar imágenes para construir un control deslizante, la **BackgroundImage** se usa para la imagen del control deslizante principal. **ThumbImage** representa el control deslizante real y se puede desplazar mediante el mouse. En el control deslizante **thumbImage** hay una línea invisible en la que se muestra la imagen de fondo en un lado de la línea y la imagen de primer plano se muestra en el otro lado.

Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo. Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.

Si el atributo en **mosaico** está establecido en true y la imagen de primer plano es menor que el área de primer plano del control deslizante, la imagen se organizará en mosaico horizontal o verticalmente, según el atributo **Direction** , para rellenar el espacio disponible.

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**Control deslizante. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Control deslizante. Slide**](slider-slide.md)
</dt> <dt>

[**SLIDEr. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Control deslizante. valor**](slider-value.md)
</dt> </dl>

 

 





