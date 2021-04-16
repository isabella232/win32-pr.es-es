---
title: BUTTONELEMENT. Down
description: El atributo Down especifica o recupera un valor que indica si el elemento de botón está en la posición arriba o abajo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT. Down Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699790"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT. Down

El atributo **Down** especifica o recupera un valor que indica si el elemento de botón está en la posición arriba o abajo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica que **BUTTONELEMENT** está en la posición hacia abajo.        |
| false | Predeterminada. Indica que **BUTTONELEMENT** está en la posición de arriba. |



 

## <a name="remarks"></a>Observaciones

Para que un elemento de botón permanezca en la posición hacia abajo, la configuración **rápida** debe estar establecida en true. De forma predeterminada, la **permanencia** es falsa y se omitirá cualquier intento **de establecer en** true.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT. downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





