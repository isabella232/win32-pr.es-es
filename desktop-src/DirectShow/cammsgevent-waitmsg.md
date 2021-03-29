---
description: El método WaitMsg espera a que se señale el evento y envía los mensajes enviados.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Método CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660438"
---
# <a name="cammsgeventwaitmsg-method"></a>CAMMsgEvent. WaitMsg, método

El `WaitMsg` método espera a que se señale el evento y envía los mensajes enviados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

Valor opcional de tiempo de espera, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el evento está señalado, o **false** si se ha producido el tiempo de espera.

## <a name="remarks"></a>Observaciones

Este método llama a la función PeekMessage para procesar los mensajes. Llame a este método en lugar de [**CAMEvent:: wait**](camevent-wait.md) si el subproceso necesita procesar mensajes mientras espera un evento. Si el subproceso no procesa los mensajes y otro subproceso envía un mensaje, podría producirse un interbloqueo.

Por ejemplo, suponga que crea un subproceso y, a continuación, se bloquea hasta que se inicializa el subproceso. Si el subproceso envía un mensaje a la ventana mediante una llamada a la función SendMessage, se producirá un interbloqueo. Esto se debe a que SendMessage no devuelve ningún resultado hasta que se haya procesado el mensaje. La llamada a WaitMsg permite que la llamada SendMessage devuelva, lo que impide el interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




