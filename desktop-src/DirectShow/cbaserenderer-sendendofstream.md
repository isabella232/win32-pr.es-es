---
description: Si se alcanzó el final de la secuencia, el método SendEndOfStream programa un evento EC \_ COMPLETE para el administrador de gráficos de filtros.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Método CBaseRenderer.SendEndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254457"
---
# <a name="cbaserenderersendendofstream-method"></a>Método CBaseRenderer.SendEndOfStream

Si se alcanzó el final del flujo, el `SendEndOfStream` método programa un evento EC COMPLETE para el administrador de \_ gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El administrador de gráficos de filtros no acepta notificaciones de eventos.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

El filtro podría recibir una notificación de fin de flujo antes de la hora de detenerse del ejemplo actual. Si es así, el filtro debe esperar antes de publicar una [**notificación EC \_ COMPLETE**](ec-complete.md) en el administrador de gráficos de filtros.

Por lo tanto:

-   Si el filtro ha recibido una notificación de fin de secuencia (EOS) temprana, este método programa un evento de temporizador. Cuando se activa el evento de temporizador, el filtro publica el evento EC \_ COMPLETE.
-   Si el filtro ha recibido una notificación de EOS que no era temprana, este método publica el evento EC \_ COMPLETE inmediatamente.
-   Si el filtro no tiene ninguna notificación EOS pendiente, el método devuelve sin hacer nada.

El método de devolución de llamada del temporizador [**es CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md). Para entregar el evento \_ EC COMPLETE, el filtro llama al [**método CBaseRenderer::NotifyEndOfStream.**](cbaserenderer-notifyendofstream.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




