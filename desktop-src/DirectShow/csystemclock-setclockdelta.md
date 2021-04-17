---
description: 'El método SetClockDelta ajusta la hora de reloj. Este método implementa el método IAMClockAdjust:: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Método CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660167"
---
# <a name="csystemclocksetclockdelta-method"></a>CSystemClock. SetClockDelta, método

El `SetClockDelta` método ajusta la hora de reloj. Este método implementa el método [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtDelta* 
</dt> <dd>

Especifica la cantidad por la que se va a ajustar el reloj, como un valor de [**\_ tiempo de referencia**](reference-time.md) . Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ un código de error de correcto o **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método simplemente llama a [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Los valores de hora devueltos por [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentan de forma continuada. Si vuelve a establecer el reloj, **getTime** continúa notificando la hora anterior hasta que el reloj interno se pone al día.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Clase CSystemClock<br/>                                                                                                                                                              |
| Encabezado<br/>  | <dl> <dt>Sysclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




