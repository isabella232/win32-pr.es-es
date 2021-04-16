---
description: El método SignalTimerFired borra el identificador del temporizador que se usa para programar la representación.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671671"
---
# <a name="cbaserenderersignaltimerfired-method"></a>CBaseRenderer. SignalTimerFired, método

El `SignalTimerFired` método borra el identificador del temporizador que se usa para programar la representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro llama a este método cuando se activa el temporizador de representación (vea [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o cuando se cancela el temporizador (vea [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)). El método restablece la variable miembro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




