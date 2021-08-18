---
title: SLIDER.value
description: El atributo value especifica o recupera la posición actual del control deslizante. | SLIDER.value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- SLIDER.value Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f9ae7c0dc45f3a14cad2aa5b7332b037302b6658043233bbd98b1d99a12e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118633"
---
# <a name="slidervalue"></a>SLIDER.value

El **atributo** value especifica o recupera la posición actual del control deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura **y** escritura **(float)** con un valor predeterminado de **min.**

## <a name="remarks"></a>Comentarios

El **valor** siempre debe ser mayor o igual que **min** y menor o igual que **max.** Si especifica un valor fuera de este intervalo, **el** valor y la posición del control deslizante no se cambian.

Vea **CUSTOMSLIDER**. [Atributo positionImage](customslider-positionimage.md) para un ejemplo que ilustra cómo se usan los atributos del **elemento SLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> </dl>

 

 





