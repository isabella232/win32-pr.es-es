---
description: El método SetTimeDelta ajusta la hora interna del reloj.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock. SetTimeDelta (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671526"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>CBaseReferenceClock. SetTimeDelta, método

El `SetTimeDelta` método ajusta la hora interna del reloj.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimeDelta* \[ CLI\]
</dt> <dd>

Cantidad para ajustar la hora del reloj, en unidades de 100-nanosegundos. Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

La clase derivada puede usar este método para ajustar el reloj interno, si se desplaza desde el dispositivo que está proporcionando información de tiempo.

El método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) nunca devuelve valores decrecientes. Si ajusta el reloj hacia atrás, **getTime** devuelve el valor anterior hasta que el reloj llega a ese valor de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




