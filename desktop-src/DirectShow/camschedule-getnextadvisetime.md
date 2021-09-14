---
description: El método GetNextAdviseTime recupera la hora de la siguiente solicitud de aviso.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Método CAMSchedule.GetNextAdviseTime (Dsschedule.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160275"
---
# <a name="camschedulegetnextadvisetime-method"></a>Método CAMSchedule.GetNextAdviseTime

El `GetNextAdviseTime` método recupera la hora de la siguiente solicitud de aviso.

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia de la siguiente solicitud de notificación o MAX \_ TIME no se programa ninguna solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




