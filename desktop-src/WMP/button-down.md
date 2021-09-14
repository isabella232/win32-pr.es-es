---
title: BUTTON.down
description: El atributo down especifica o recupera un valor que indica si button está en la posición arriba o abajo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- Button.down Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889492"
---
# <a name="buttondown"></a>BUTTON.down

El **atributo** down especifica o recupera un valor que indica si **button** está en la posición arriba o abajo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                                   |
|-------|---------------------------------------------------------------|
| true  | Indica que button **está** en la posición de abajo.        |
| false | Predeterminada. Indica que button **está** en la posición de arriba. |



 

## <a name="remarks"></a>Observaciones

Para que **button** permanezca en la posición de abajo, el valor **de sticky** debe establecerse en true. De forma predeterminada, **sticky** es false y cualquier intento de establecer **en** true se omitirá.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON.downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





