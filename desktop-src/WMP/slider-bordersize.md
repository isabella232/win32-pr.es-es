---
title: SLIDEr. Border
description: El atributo de borde especifica o recupera el ancho del borde en píxeles.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Control deslizante. bordes de Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660896"
---
# <a name="sliderbordersize"></a>SLIDEr. Border

El atributo de **borde** especifica o recupera el ancho del borde en píxeles.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (**Long**) que representa el ancho del borde en píxeles. El valor predeterminado es cero.

## <a name="remarks"></a>Observaciones

Este atributo define un desplazamiento desde el principio y el final del control deslizante que es, desde la izquierda y la derecha si el atributo **Direction** se establece en "horizontal" y desde la parte superior e inferior si se establece en "vertical". Estas posiciones de desplazamiento dictan las posiciones mínima y máxima del control deslizante, más allá del que no se aplicará el color de primer plano o la imagen.

Si se usa una imagen de fondo con el atributo en **mosaico** establecido en true, el desplazamiento se aplica a la imagen, lo que indica la cantidad de la imagen (desde la izquierda y la derecha o desde la parte superior e inferior) que se va a usar para los bordes inicial y final del control deslizante, con la parte central de la imagen que se coloca en mosaico en el resto. De esta manera, se puede usar una imagen de fondo pequeña para cubrir la longitud total de un control deslizante más grande.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDEr. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Control deslizante. en mosaico**](slider-tiled.md)
</dt> </dl>

 

 





