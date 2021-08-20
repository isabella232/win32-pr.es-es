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
ms.openlocfilehash: 990291f8b618032d3e5b7e33a7644735cf1673482b2190936f2e496dbf68bd64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933443"
---
# <a name="textscrolling"></a>TEXT.scrolling

El **atributo scrolling** especifica o recupera un valor que indica si el texto se desplaza.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valor | Descripción                     |
|-------|---------------------------------|
| true  | El desplazamiento está habilitado.           |
| false | Predeterminada. El desplazamiento está deshabilitado. |



 

## <a name="remarks"></a>Comentarios

La característica de desplazamiento proporciona un búfer de dos espacios entre el final del texto y el principio de la línea repetida.

El **atributo de** justificación especifica dónde aparece primero el texto antes de que comience el desplazamiento.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

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

 

 





