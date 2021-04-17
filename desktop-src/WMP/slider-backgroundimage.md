---
title: Control deslizante. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo del control deslizante.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Control deslizante. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660218"
---
# <a name="sliderbackgroundimage"></a>Control deslizante. backgroundImage

El atributo **BackgroundImage** especifica o recupera la imagen de fondo del control deslizante.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Al usar imágenes para construir un control deslizante, la **BackgroundImage** se usa para la imagen del control deslizante principal. **ThumbImage** representa el control deslizante real y se puede desplazar mediante el mouse. En el control deslizante **thumbImage** hay una línea invisible en la que se muestra la imagen de fondo en un lado de la línea y la imagen de primer plano se muestra en el otro lado.

Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo. Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.

Si el atributo en **mosaico** está establecido en true y la imagen de fondo es más pequeña que el control deslizante, la imagen se organizará en mosaico horizontal o verticalmente según el atributo **Direction** . Si el atributo de **borde** se establece en un valor mayor que cero, el número especificado será el número de píxeles desde la izquierda, la derecha o la parte superior e inferior de la imagen (de nuevo, según el atributo de **Dirección** ) que se reservará para los bordes del control deslizante. En este caso, solo se usa la parte central de la imagen para colocar en mosaico el resto del control.

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**Control deslizante. Slide**](slider-slide.md)
</dt> <dt>

[**SLIDEr. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





