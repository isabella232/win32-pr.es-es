---
description: El método TimerCallback es un método de devolución de llamada para el evento de temporizador de fin de secuencia.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer.TimerCallback (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061756"
---
# <a name="cbaserenderertimercallback-method"></a>CBaseRenderer.TimerCallback (método)

El método es un método de devolución de llamada para el evento de temporizador de fin `TimerCallback` de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El [**método CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento de temporizador para programar notificaciones EC \_ COMPLETE. El **método CBaseRenderer::TimerCallback** es la función de devolución de llamada para el evento de temporizador. El método llama de nuevo a `TimerCallback` **SendEndOfStream** y **SendEndOfStream** determina si se debe enviar la notificación EC \_ COMPLETE o establecer otro temporizador.

El [**método CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela el evento de temporizador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




