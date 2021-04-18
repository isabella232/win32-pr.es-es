---
description: El método GetNextAdviseTime recupera la hora de la solicitud de notificación siguiente.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Método CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671112"
---
# <a name="camschedulegetnextadvisetime-method"></a>CAMSchedule. GetNextAdviseTime, método

El `GetNextAdviseTime` método recupera la hora de la solicitud de notificación siguiente.

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia de la solicitud de notificación siguiente o el tiempo máximo que \_ no hay solicitudes programadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule. h (incluir streams. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




