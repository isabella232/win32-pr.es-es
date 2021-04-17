---
title: Control deslizante. valor
description: El atributo value especifica o recupera la posición actual del control deslizante. | Control deslizante. valor
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Control deslizante. Value Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660547"
---
# <a name="slidervalue"></a>Control deslizante. valor

El atributo **Value** especifica o recupera la posición actual del control deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor predeterminado de **min**.

## <a name="remarks"></a>Observaciones

El **valor** siempre debe ser mayor o igual que **min** y menor o igual que **Max**. Si especifica un valor fuera de este intervalo, el **valor** y la posición del control deslizante no cambian.

Vea **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. min**](slider-min.md)
</dt> </dl>

 

 





