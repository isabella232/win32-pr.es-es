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
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241022"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

El **atributo crossFade** especifica o recupera un valor que indica si está habilitada la atenuación cruzada.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                      |
|-------|----------------------------------|
| true  | El atenuado cruzado está habilitado.           |
| false | Predeterminada. La atenuación cruzada está deshabilitada. |



 

## <a name="remarks"></a>Observaciones

El atenuado cruzado es una característica de procesamiento de audio que reduce gradualmente el volumen de un elemento multimedia cerca del final de su reproducción mientras se inicia simultáneamente la reproducción del siguiente elemento multimedia en el volumen mínimo y aumenta gradualmente al volumen normal. El atributo **crossFadeWindow** especifica la superposición entre el inicio del segundo elemento multimedia y el final del primer elemento multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





