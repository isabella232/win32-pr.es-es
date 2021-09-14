---
description: El método SignalTimerFired borra el identificador de temporizador usado para programar la representación.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer.SignalTimerFired (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061761"
---
# <a name="cbaserenderersignaltimerfired-method"></a>CBaseRenderer.SignalTimerFired (método)

El `SignalTimerFired` método borra el identificador de temporizador utilizado para programar la representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro llama a este método cuando se activa el temporizador de representación (vea [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o cuando se cancela el temporizador (vea [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)). El método restablece la variable [**miembro CBaseRenderer::m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) a cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




