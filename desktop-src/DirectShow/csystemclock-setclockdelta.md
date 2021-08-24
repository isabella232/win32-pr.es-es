---
description: El método SetClockDelta ajusta la hora del reloj. Este método implementa el método IAMClockAdjust::SetClockDelta.
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Método CSystemClock.SetClockDelta (Sysclock.h)
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
ms.openlocfilehash: c98ccf35e41886594a3aab8c3abec6737128d8d7e22f6dfb75d0ac88ac3b7a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538665"
---
# <a name="csystemclocksetclockdelta-method"></a>Método CSystemClock.SetClockDelta

El `SetClockDelta` método ajusta la hora del reloj. Este método implementa el [**método IAMClockAdjust::SetClockDelta.**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Rtdelta* 
</dt> <dd>

Especifica la cantidad por la que se va a ajustar el reloj, como un [**valor DE HORA \_ DE**](reference-time.md) REFERENCIA. Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método simplemente llama [**a CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Los valores de hora devueltos [**por IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentan de forma monótica. Si vuelve a establecer el reloj, **GetTime** continúa informando de la hora anterior hasta que el reloj interno se activa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | CSystemClock (clase)<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Sysclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




