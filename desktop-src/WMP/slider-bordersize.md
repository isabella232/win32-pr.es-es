---
title: SLIDER.borderSize
description: El atributo borderSize especifica o recupera el ancho del borde en píxeles.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- SLIDER.borderSize Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db28f97b452e46489184446daf8f15a33b77ff027b5d6117a04c72cbe9946b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832733"
---
# <a name="sliderbordersize"></a>SLIDER.borderSize

El **atributo borderSize** especifica o recupera el ancho del borde en píxeles.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura **y** escritura **(long)** que representa el ancho del borde en píxeles. El valor predeterminado es cero.

## <a name="remarks"></a>Comentarios

Este atributo define un desplazamiento desde el principio y el final del  control deslizante, es decir, desde la izquierda y la derecha si el atributo de dirección se establece en "horizontal", y desde la parte superior e inferior si se establece en "vertical". Estas posiciones de desplazamiento dictan las posiciones mínima y máxima del control deslizante, más allá de las cuales no se aplicará el color de primer plano o la imagen.

Si se usa una  imagen de fondo con el atributo en mosaico establecido en true, el desplazamiento se aplica a la imagen, dictando la cantidad de la imagen (ya sea desde la izquierda y la derecha o desde la parte superior e inferior) que se usará para los bordes inicial y final del control deslizante, con la parte central de la imagen en mosaico en todo el resto. De este modo, se puede usar una imagen de fondo pequeña para cubrir toda la longitud de un control deslizante mayor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER.tiled**](slider-tiled.md)
</dt> </dl>

 

 





