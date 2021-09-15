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
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258775"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER.value

El **atributo** value especifica o recupera la posición actual del control deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor predeterminado igual al **atributo min.**

## <a name="remarks"></a>Observaciones

El **valor** debe ser mayor o igual que **min** y menor o igual que **max.** Si el valor está fuera del intervalo, se emite una advertencia y el valor no cambia.

## <a name="examples"></a>Ejemplos

Vea el [atributo positionImage](customslider-positionimage.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento CUSTOMSLIDER.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





