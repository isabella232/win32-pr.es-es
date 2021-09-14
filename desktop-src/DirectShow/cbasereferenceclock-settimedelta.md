---
description: El método SetTimeDelta ajusta la hora del reloj interno.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock.SetTimeDelta (Refclock.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070131"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Método CBaseReferenceClock.SetTimeDelta

El `SetTimeDelta` método ajusta la hora del reloj interno.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimeDelta* \[ Ref\]
</dt> <dd>

Cantidad para ajustar la hora del reloj, en unidades de 100 nanosegundos. Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

La clase derivada puede usar este método para ajustar el reloj interno, si se desvia del dispositivo que proporciona información de tiempo.

El [**método CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) nunca devuelve valores decrecientes. Si ajusta el reloj hacia atrás, **GetTime** devuelve el valor anterior hasta que el reloj vuelve a alcanzar ese valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




