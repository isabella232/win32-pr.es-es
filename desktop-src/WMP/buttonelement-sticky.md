---
title: BUTTONELEMENT.sticky
description: El atributo permanente especifica o recupera un valor que indica si BUTTONELEMENT es un botón de alternancia, es decir, si es un botón de dos estados o de un solo estado.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- ButtonELEMENT.sticky Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8a709fc28f0d1529c58725db5856931195a66cc370559dd9d14af61e869db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120061"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT.sticky

El **atributo** permanente especifica o recupera un valor que indica si **BUTTONELEMENT** es un botón de alternancia, es decir, si es un botón de dos estados o de un solo estado.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** es permanente.              |
| false | Predeterminada. **BUTTONELEMENT** no es permanente. |



 

## <a name="remarks"></a>Comentarios

Si el **atributo permanente** se establece en true, el elemento de botón cambiará al estado anterior cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic en él. Cuando el elemento button está en estado down, el atributo **down** será true y se mostrará la parte adecuada del grupo de botones **downImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





