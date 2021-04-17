---
description: El método TimerCallback es un método de devolución de llamada para el evento de temporizador de final de secuencia.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661265"
---
# <a name="cbaserenderertimercallback-method"></a>CBaseRenderer. TimerCallback, método

El `TimerCallback` método es un método de devolución de llamada para el evento de temporizador de final de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento de temporizador para programar \_ notificaciones completas de EC. El método **CBaseRenderer:: TimerCallback** es la función de devolución de llamada para el evento del temporizador. El `TimerCallback` método llama a **SendEndOfStream** de nuevo y **SendEndOfStream** determina si se debe enviar la notificación de finalización de EC \_ o establecer otro temporizador.

El método [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela el evento del temporizador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




