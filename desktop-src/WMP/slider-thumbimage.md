---
title: SLIDER.thumbImage
description: El atributo thumbImage especifica o recupera la imagen que se usará para representar la posición actual del control deslizante.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- SLIDER.thumbImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0711cb7a652032db4b167040fbd604d1e561885926bf8fc7c31d1fedb65049e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995145"
---
# <a name="sliderthumbimage"></a>SLIDER.thumbImage

El **atributo thumbImage** especifica o recupera la imagen que se usará para representar la posición actual del control deslizante.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene el nombre de un archivo de imagen.

## <a name="remarks"></a>Comentarios

ThumbImage **especifica** la imagen que se usará para representar la posición actual, así como indica que el usuario puede tomar medidas con el control . Si no se especifica ninguna imagen de posición, el control deslizante no es interactivo.

La imagen del control deslizante se centra en la dimensión estrecha del control deslizante. Si la imagen de posición es más estrecha que el control, la imagen aparece en el centro del fondo. Si la imagen thumb es mayor que el control , los extremos de la imagen se cortan.

La posición del control deslizante se especifica mediante el centro de la imagen digital. Si **borderSize** es cero, solo se podrá ver la mitad de la imagen del control deslizante en las posiciones del control deslizante inicial y final. Para evitar esto, establezca **borderSize** en un valor mayor o igual que la  mitad del ancho de la imagen digital (o la mitad del alto si la dirección está establecida en "vertical").

Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir GIF animados).

Vea **CUSTOMSLIDER**. [Atributo positionImage](customslider-positionimage.md) para un ejemplo que ilustra cómo se usan los atributos del **elemento SLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER.direction**](slider-direction.md)
</dt> </dl>

 

 





