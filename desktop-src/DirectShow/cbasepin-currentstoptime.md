---
description: 'El método CurrentStopTime recupera la hora de detención del segmento, establecida por el método CBasePin:: NewSegment.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Método CBasePin. CurrentStopTime (Amfilter. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660608"
---
# <a name="cbasepincurrentstoptime-method"></a>CBasePin. CurrentStopTime, método

El `CurrentStopTime` método recupera la hora de detención del segmento, establecida por el método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




