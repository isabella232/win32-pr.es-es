---
title: Control deslizante. backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo del control deslizante.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- CONTROL SLIDEr. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660220"
---
# <a name="sliderbackgroundcolor"></a>Control deslizante. backgroundColor

El atributo **BackgroundColor** especifica o recupera el color de fondo del control deslizante.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Un control deslizante básico se puede construir especificando **BackgroundColor** o **BackgroundImage**, y **foregroundColor** o **foregroundImage**.

Al usar los colores, las dimensiones del control deslizante definen el área rellenada por el color de fondo. El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.

Para hacer un relleno de degradado del área ocupada por el color de fondo o de primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor** .

Vea *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**Control deslizante. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDEr. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDEr. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





