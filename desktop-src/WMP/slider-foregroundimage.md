---
title: SLIDER.foregroundImage
description: El atributo foregroundImage especifica o recupera la imagen de primer plano del control deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- SLIDER.foregroundImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735715"
---
# <a name="sliderforegroundimage"></a>SLIDER.foregroundImage

El **atributo foregroundImage** especifica o recupera la imagen de primer plano del control deslizante.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Cuando se usan imágenes para construir un control deslizante, **backgroundImage** se usa para la imagen del control deslizante principal. **ThumbImage representa** el control deslizante real y se puede mover con el mouse. En el **control deslizante thumbImage** hay una línea invisible donde la imagen de fondo se muestra en un lado de la línea y la imagen de primer plano se muestra en el otro lado.

Cuando el **control deslizante thumbImage** se  mueve con el mouse, si la diapositiva está establecida en true, la imagen de primer plano se desliza como si el control deslizante lo extrayes para cubrir la imagen de fondo. Si **la** diapositiva se establece en false, la imagen de primer plano no se mueve, pero se muestra en su lugar, como si el control deslizante mueve la imagen de fondo fuera de la imagen de primer plano.

Si el atributo **en** mosaico se establece en true y la imagen de primer plano es menor que el  área de primer plano del control deslizante, la imagen se mosaico horizontal o verticalmente, dependiendo del atributo de dirección, para rellenar el espacio disponible.

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





