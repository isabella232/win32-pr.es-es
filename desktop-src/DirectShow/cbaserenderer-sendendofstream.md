---
description: Si se ha alcanzado el final de la secuencia, el método SendEndOfStream programa un \_ evento EC complete para el administrador de gráficos de filtro.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Método CBaseRenderer. SendEndOfStream (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670667"
---
# <a name="cbaserenderersendendofstream-method"></a>CBaseRenderer. SendEndOfStream, método

Si se ha alcanzado el final de la secuencia, el `SendEndOfStream` método programa un \_ evento EC complete para el administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El administrador de gráficos de filtro no acepta notificaciones de eventos.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

El filtro podría recibir una notificación de final de secuencia antes de la hora de detención del ejemplo actual. Si es así, el filtro debe esperar antes de publicar una notificación de [**\_ finalización de EC**](ec-complete.md) en el administrador de gráficos de filtro.

Por lo tanto:

-   Si el filtro ha recibido una notificación de final de secuencia (EOS) temprana, este método programa un evento de temporizador. Cuando se activa el evento de temporizador, el filtro envía el \_ evento de finalización de EC.
-   Si el filtro ha recibido una notificación de EOS que no era temprano, este método publica el \_ evento de finalización de EC inmediatamente.
-   Si el filtro no tiene ninguna notificación de EOS pendiente, el método devuelve sin hacer nada.

El método de devolución de llamada del temporizador es [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md). Para enviar el \_ evento de finalización de EC, el filtro llama al método [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




