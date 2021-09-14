---
description: El método CurrentStopTime recupera la hora de detención del segmento, establecida por el método CBasePin::NewSegment.
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Método CBasePin.CurrentStopTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061359"
---
# <a name="cbasepincurrentstoptime-method"></a>Método CBasePin.CurrentStopTime

El `CurrentStopTime` método recupera el tiempo de detención del segmento, establecido por el método [**CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




