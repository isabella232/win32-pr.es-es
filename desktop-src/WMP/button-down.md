---
title: BOTÓN. abajo
description: El atributo Down especifica o recupera un valor que indica si el botón está en la posición arriba o abajo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BOTÓN. bajar ventanas Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699766"
---
# <a name="buttondown"></a>BOTÓN. abajo

El atributo **Down** especifica o recupera un valor que indica si el **botón** está en la posición arriba o abajo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                   |
|-------|---------------------------------------------------------------|
| true  | Indica que el **botón** está en la posición hacia abajo.        |
| false | Predeterminada. Indica que el **botón** está en la posición arriba. |



 

## <a name="remarks"></a>Observaciones

Para que un **botón** permanezca en la posición hacia abajo **, se** debe establecer en true. De forma predeterminada, la **permanencia** es falsa y se omitirá cualquier intento **de establecer en** true.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON. downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





