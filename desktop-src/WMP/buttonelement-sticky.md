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
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889305"
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



 

## <a name="remarks"></a>Observaciones

Si el **atributo permanente** se establece en true, el elemento de botón cambiará al estado anterior cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic en él. Cuando el elemento button está en estado down, el atributo **down** será true y se mostrará la parte adecuada del grupo de botones **downImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





