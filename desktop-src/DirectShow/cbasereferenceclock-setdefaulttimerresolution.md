---
description: El método SetDefaultTimerResolution establece la resolución del temporizador del reloj de referencia.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Método CBaseReferenceClock. SetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671529"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>CBaseReferenceClock. SetDefaultTimerResolution, método

El `SetDefaultTimerResolution` método establece la resolución del temporizador del reloj de referencia.

## <a name="syntax"></a>Sintaxis


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*timerResolution* 
</dt> <dd>

Resolución mínima del temporizador, en unidades de 100-nanosegundos. Si el valor es cero, el reloj de referencia cancela su solicitud anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método implementa el método [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




