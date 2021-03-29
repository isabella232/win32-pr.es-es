---
description: El método GetDefaultTimerResolution devuelve la resolución actual del temporizador del reloj de referencia.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Método CBaseReferenceClock. GetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660589"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>CBaseReferenceClock. GetDefaultTimerResolution, método

El `GetDefaultTimerResolution` método devuelve la resolución actual del temporizador del reloj de referencia.

## <a name="syntax"></a>Sintaxis


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimerResolution* 
</dt> <dd>

Recibe la resolución del temporizador solicitada, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método implementa el método [**IReferenceClockTimerControl:: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




