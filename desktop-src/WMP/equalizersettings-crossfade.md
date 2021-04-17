---
title: EQUALIZERSETTINGS. encadenado
description: El atributo encadenado especifica o recupera un valor que indica si está habilitado el fundido cruzado.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. encadenado de Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700306"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS. encadenado

El atributo **encadenado** especifica o recupera un valor que indica si está habilitado el fundido cruzado.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                      |
|-------|----------------------------------|
| true  | La transición transversal está habilitada.           |
| false | Predeterminada. La transición transversal está deshabilitada. |



 

## <a name="remarks"></a>Observaciones

El fundido cruzado es una característica de procesamiento de audio que reduce gradualmente el volumen de un elemento multimedia cerca del final de la reproducción, al mismo tiempo que inicia la reproducción del siguiente elemento multimedia en el volumen mínimo y lo incrementa gradualmente al volumen normal. El atributo **crossFadeWindow** especifica la superposición entre el inicio del segundo elemento multimedia y el final del primer elemento multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





