---
title: SLIDEr. foregroundColor
description: El atributo foregroundColor especifica o recupera el color de primer plano del control deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- CONTROL SLIDEr. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661193"
---
# <a name="sliderforegroundcolor"></a>SLIDEr. foregroundColor

El atributo **foregroundColor** especifica o recupera el color de primer plano del control deslizante.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer. El valor predeterminado es "blanco".

## <a name="remarks"></a>Observaciones

Un control deslizante básico se puede construir especificando uno de los dos pares de atributos: **BackgroundColor** y **foregroundColor**, o el argumento **BackgroundImage** y **foregroundImage**.

Cuando se construye un control deslizante con los atributos de color, las dimensiones del control deslizante definen el área rellenada por el color de fondo. El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.

Para hacer un relleno de degradado en el área ocupada por el color de fondo o de primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor** .

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

[**Control deslizante. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDEr. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDEr. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDEr. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





