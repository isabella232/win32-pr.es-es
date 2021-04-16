---
title: BUTTONELEMENT. adhesiva
description: El atributo de permanencia especifica o recupera un valor que indica si BUTTONELEMENT es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT. Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699800"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT. adhesiva

El atributo de **permanencia** especifica o recupera un valor que indica si **BUTTONELEMENT** es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** es permanente.              |
| false | Predeterminada. **BUTTONELEMENT** no es permanente. |



 

## <a name="remarks"></a>Observaciones

Si el atributo de **permanencia** está establecido en true, el elemento de botón cambiará al estado desactivado cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic. Cuando el elemento de botón está inactivo, el atributo **Down** será true y se mostrará la parte adecuada del grupo de botones **downImage** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT. Down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





