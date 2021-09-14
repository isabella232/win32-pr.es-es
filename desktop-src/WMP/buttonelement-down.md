---
title: BUTTONELEMENT.down
description: El atributo down especifica o recupera un valor que indica si el elemento de botón está en la posición de arriba o abajo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- ButtonELEMENT.down Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889345"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT.down

El **atributo** down especifica o recupera un valor que indica si el elemento de botón está en la posición de arriba o abajo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica que **BUTTONELEMENT** está en la posición de abajo.        |
| false | Predeterminada. Indica que **BUTTONELEMENT** está en la posición hacia arriba. |



 

## <a name="remarks"></a>Observaciones

Para que un elemento de botón permanezca en la posición de abajo, **sticky** debe establecerse en true. De forma predeterminada, **sticky** es false y cualquier intento de establecer **en** true se omitirá.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





