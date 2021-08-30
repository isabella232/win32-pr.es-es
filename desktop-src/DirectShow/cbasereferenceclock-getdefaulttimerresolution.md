---
description: El método GetDefaultTimerResolution devuelve la resolución actual del temporizador del reloj de referencia.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Método CBaseReferenceClock.GetDefaultTimerResolution (Refclock.h)
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
ms.openlocfilehash: dbd3eb192839d6957af9fb63c32a1b1dcbb3a5c386c47d2f66408ec63d7cba21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076575"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>CBaseReferenceClock.GetDefaultTimerResolution (método)

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

Recibe la resolución de temporizador solicitada, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método implementa el [**método IReferenceClockTimerControl::GetDefaultTimerResolution.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




