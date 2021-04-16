---
description: El método TriggerThread reactiva el subproceso de trabajo que controla la programación.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Método CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671525"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>CBaseReferenceClock. TriggerThread, método

El `TriggerThread` método reactiva el subproceso de trabajo que controla la programación.

## <a name="syntax"></a>Sintaxis


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El reloj usa un subproceso de trabajo que llama al método [**CAMSchedule:: Advise**](camschedule-advise.md) en los momentos adecuados. La clase derivada puede llamar `TriggerThread` a para reactivar el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




