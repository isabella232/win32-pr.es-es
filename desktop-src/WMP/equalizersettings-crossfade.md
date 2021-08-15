---
title: EQUALIZERSETTINGS.crossFade
description: El atributo crossFade especifica o recupera un valor que indica si está habilitada la atenuación cruzada.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS.crossFade Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff38ee7634f31da7717bfca015ebaacd88796d9c8186faef155704a449bbb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838630"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

El **atributo crossFade** especifica o recupera un valor que indica si está habilitada la atenuación cruzada.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valor | Descripción                      |
|-------|----------------------------------|
| true  | El atenuado cruzado está habilitado.           |
| false | Predeterminada. La atenuación cruzada está deshabilitada. |



 

## <a name="remarks"></a>Comentarios

El atenuado cruzado es una característica de procesamiento de audio que reduce gradualmente el volumen de un elemento multimedia cerca del final de su reproducción mientras se inicia simultáneamente la reproducción del siguiente elemento multimedia en el volumen mínimo y aumenta gradualmente al volumen normal. El atributo **crossFadeWindow** especifica la superposición entre el inicio del segundo elemento multimedia y el final del primer elemento multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





