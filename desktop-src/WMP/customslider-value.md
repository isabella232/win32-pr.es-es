---
title: CUSTOMSLIDER. Value
description: El atributo value especifica o recupera la posición actual del control deslizante. | CUSTOMSLIDER. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- CUSTOMSLIDER. Value Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700120"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER. Value

El atributo **Value** especifica o recupera la posición actual del control deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor predeterminado igual al atributo **min** .

## <a name="remarks"></a>Observaciones

El **valor** debe ser mayor o igual que **min** y menor o igual que **Max**. Si el valor está fuera del intervalo, se emite una advertencia y el valor no cambia.

## <a name="examples"></a>Ejemplos

Vea el atributo [positionImage](customslider-positionimage.md) para ver un ejemplo que ilustra cómo se usan los atributos del elemento **CUSTOMSLIDER** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





