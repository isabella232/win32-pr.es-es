---
title: CUSTOMSLIDER.value
description: El atributo value especifica o recupera la posición actual del control deslizante. | CUSTOMSLIDER.value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- CustomSLIDER.value Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a256274fe2170ad50c164f7bf6768f82e3266db7a4ea5e2c6c8e28edd083c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579713"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER.value

El **atributo** value especifica o recupera la posición actual del control deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura **y** escritura **(float)** con un valor predeterminado igual al **atributo min.**

## <a name="remarks"></a>Comentarios

El **valor** debe ser mayor o igual que **min** y menor o igual que **max.** Si el valor queda fuera del intervalo, se emite una advertencia y el valor no cambia.

## <a name="examples"></a>Ejemplos

Vea el [atributo positionImage](customslider-positionimage.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento CUSTOMSLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





