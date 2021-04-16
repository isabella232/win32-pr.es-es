---
title: TEXTO. desplazamiento
description: El atributo de desplazamiento especifica o recupera un valor que indica si el texto se desplaza.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. Scrolling Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718779"
---
# <a name="textscrolling"></a>TEXTO. desplazamiento

El atributo de **desplazamiento** especifica o recupera un valor que indica si el texto se desplaza.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                     |
|-------|---------------------------------|
| true  | El desplazamiento está habilitado.           |
| false | Predeterminada. El desplazamiento está deshabilitado. |



 

## <a name="remarks"></a>Observaciones

La característica de desplazamiento proporciona un búfer de dos espacios entre el final del texto y el principio de la línea repetida.

El atributo **justificación** especifica dónde aparece el texto primero antes de que se inicie el desplazamiento.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXTO. justificación**](text-justification.md)
</dt> <dt>

[**TEXT. scrollingAmount**](text-scrollingamount.md)
</dt> <dt>

[**TEXT. scrollingDelay**](text-scrollingdelay.md)
</dt> <dt>

[**TEXT. scrollingDirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





