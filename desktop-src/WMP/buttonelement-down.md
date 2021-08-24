---
title: BUTTONELEMENT.down
description: El atributo down especifica o recupera un valor que indica si el elemento button está en la posición arriba o abajo.
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
ms.openlocfilehash: ff20aebda01b24dc14eb7d5298ee0d663d903bedcb7ef6ef8b05b6211af8b567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764475"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT.down

El **atributo** down especifica o recupera un valor que indica si el elemento button está en la posición arriba o abajo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Valor | Descripción                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica que **BUTTONELEMENT** está en la posición de abajo.        |
| false | Predeterminada. Indica que **BUTTONELEMENT** está en la posición de arriba. |



 

## <a name="remarks"></a>Comentarios

Para que un elemento de botón permanezca en la posición de abajo, **sticky** debe establecerse en true. De forma predeterminada, **sticky** es false y cualquier intento de establecer **en** true se omitirá.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





