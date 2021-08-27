---
description: El método SetDefaultTimerResolution establece la resolución del temporizador del reloj de referencia.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Método CBaseReferenceClock.SetDefaultTimerResolution (Refclock.h)
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
ms.openlocfilehash: 980f31856aba14079da0f5b9625dca40846255d6f02361b2798d7c38c1cd4f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087425"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>CBaseReferenceClock.SetDefaultTimerResolution (método)

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

Resolución mínima del temporizador, en unidades de 100 nanosegundos. Si el valor es cero, el reloj de referencia cancela su solicitud anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método implementa el [**método IReferenceClockTimerControl::SetDefaultTimerResolution.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




