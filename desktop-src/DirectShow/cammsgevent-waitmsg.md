---
description: El método WaitMsg espera a que se señale el evento, mientras se envían los mensajes enviados.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Método CAMMsgEvent.WaitMsg (Wxutil.h)
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
ms.openlocfilehash: 94a2169d9938a8c2ff8a1961eee0895fefd7cc8a2dd487a4193d8053d27d98ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955454"
---
# <a name="cammsgeventwaitmsg-method"></a>Método CAMMsgEvent.WaitMsg

El `WaitMsg` método espera a que se señale el evento, mientras se envían los mensajes enviados.

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

Valor de tiempo de espera opcional, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se señala el evento o **FALSE** si se ha producido el tiempo de espera.

## <a name="remarks"></a>Comentarios

Este método llama a la función PeekMessage para procesar mensajes. Llame a este método en lugar de [**a CAMEvent::Wait**](camevent-wait.md) si el subproceso necesita procesar mensajes mientras espera un evento. Si el subproceso no procesa mensajes y otro subproceso envía un mensaje, podría producirse un interbloqueo.

Por ejemplo, suponga que crea un subproceso y, a continuación, bloquea hasta que se inicializa el subproceso. Si el subproceso envía un mensaje a la ventana mediante una llamada a la función SendMessage, se produciría un interbloqueo. Esto se debe a que SendMessage no devuelve hasta que se ha procesado el mensaje. Llamar a WaitMsg permite que se devuelva la llamada SendMessage, lo que evita el interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




