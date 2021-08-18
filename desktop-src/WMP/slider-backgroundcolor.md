---
title: SLIDER.backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo del control deslizante.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- SLIDER.backgroundColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc2de30392c58cfad151e2d3c209f0407880a47522a536bf08dbe42d7f56dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995235"
---
# <a name="sliderbackgroundcolor"></a>SLIDER.backgroundColor

El **atributo backgroundColor** especifica o recupera el color de fondo del control deslizante.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene cualquier valor de color Internet Explorer Microsoft. No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Un control deslizante básico se puede construir especificando **backgroundColor** o **backgroundImage**, **y foregroundColor** o **foregroundImage**.

Cuando se usan los colores, las dimensiones del control deslizante definen el área rellenada por el color de fondo. El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.

Para realizar un relleno de degradado del área ocupada por el color de fondo o primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor.**

Vea *CUSTOMSLIDER*. [Atributo positionImage](customslider-positionimage.md) para un ejemplo que ilustra cómo se usan los atributos del **elemento SLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





