---
title: SLIDER.foregroundColor
description: El atributo foregroundColor especifica o recupera el color de primer plano del control deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- SLIDER.foregroundColor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569098"
---
# <a name="sliderforegroundcolor"></a>SLIDER.foregroundColor

El **atributo foregroundColor** especifica o recupera el color de primer plano del control deslizante.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene cualquier valor de color Internet Explorer microsoft. El valor predeterminado es "white".

## <a name="remarks"></a>Comentarios

Un control deslizante básico se puede construir especificando uno de los dos pares de atributos: **backgroundColor** y **foregroundColor**, o **backgroundImage** y **foregroundImage**.

Al construir un control deslizante con los atributos de color, las dimensiones del control deslizante definen el área rellenada por el color de fondo. El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.

Para rellenar un degradado en el área ocupada por el color de fondo o primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor.**

Vea *CUSTOMSLIDER*. [Atributo positionImage](customslider-positionimage.md) para un ejemplo que ilustra cómo se usan los atributos del **elemento SLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de color**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





