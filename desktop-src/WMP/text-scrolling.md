---
title: TEXT.scrolling
description: El atributo de desplazamiento especifica o recupera un valor que indica si el texto se desplaza.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- Text.scrolling Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568545"
---
# <a name="textscrolling"></a>TEXT.scrolling

El **atributo de** desplazamiento especifica o recupera un valor que indica si el texto se desplaza.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                     |
|-------|---------------------------------|
| true  | El desplazamiento está habilitado.           |
| false | Predeterminada. El desplazamiento está deshabilitado. |



 

## <a name="remarks"></a>Observaciones

La característica de desplazamiento proporciona un búfer de dos espacios entre el final del texto y el principio de la línea repetida.

El **atributo de** justificación especifica dónde aparece primero el texto antes de que comience el desplazamiento.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.justification**](text-justification.md)
</dt> <dt>

[**TEXT.scrollingAmount**](text-scrollingamount.md)
</dt> <dt>

[**TEXT.scrollingDelay**](text-scrollingdelay.md)
</dt> <dt>

[**TEXT.scrollingDirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





