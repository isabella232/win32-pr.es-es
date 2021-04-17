---
title: SLIDEr. thumbImage
description: El atributo thumbImage especifica o recupera la imagen que se utilizará para representar la posición actual del control deslizante.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- CONTROL SLIDEr. thumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700103"
---
# <a name="sliderthumbimage"></a>SLIDEr. thumbImage

El atributo **thumbImage** especifica o recupera la imagen que se utilizará para representar la posición actual del control deslizante.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Observaciones

**ThumbImage** especifica la imagen que se usará para representar la posición actual, así como el modo de indicar que el usuario puede realizar una acción con el control. Si no se especifica ninguna imagen Thumb, el control deslizante no es interactivo.

La imagen Thumb está centrada en la dimensión estrecha del control deslizante. Si la imagen Thumb es más estrecha que el control, la imagen aparece en medio del fondo. Si la imagen de Thumb es mayor que el control, los extremos de la imagen se cortan.

La posición del control deslizante se especifica mediante el centro de la imagen de Thumb. Si el valor de **borde** es cero, solo la mitad de la imagen Thumb estará visible en las posiciones del control deslizante inicial y final. Para evitarlo, establezca el valor de **borde** en un valor mayor o igual que la mitad del ancho de la imagen de control de posición (o la mitad del alto si la **Dirección** está establecida en "vertical").

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).

Vea **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. Border**](slider-bordersize.md)
</dt> <dt>

[**Control deslizante. Direction**](slider-direction.md)
</dt> </dl>

 

 





