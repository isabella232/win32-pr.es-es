---
description: Procesa las solicitudes. Se trata de una función miembro virtual pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Método CMsgThread.ThreadMessageProc (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb11a7cac567bd645d0e3fd1c294636b5df9410fbc54012633ec0c0d161b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909705"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>Método CMsgThread.ThreadMessageProc

Procesa las solicitudes. Se trata de una función miembro virtual pura.

## <a name="syntax"></a>Sintaxis


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Código de solicitud.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Parámetro de marca opcional que se solicitará.

</dd> <dt>

*lpParam* 
</dt> <dd>

Puntero opcional a datos adicionales o un bloque de datos devueltos.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntero opcional a un objeto de evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cualquier valor devuelto distinto de cero hace que el subproceso se cierre. Devuelve cero a menos que se haya procesado recientemente una solicitud de salida.

## <a name="remarks"></a>Comentarios

Esta función virtual pura debe reemplazarse en la clase derivada. Se llamará una vez para cada solicitud en cola mediante una llamada a la función miembro [**CMsgThread::P utThreadMsg.**](cmsgthread-putthreadmsg.md)

La función miembro define los cuatro parámetros. Normalmente, use el *parámetro uMsg* para indicar la solicitud y los otros tres parámetros serán parámetros adicionales opcionales. La aplicación que realiza la llamada puede proporcionar un puntero a un [**objeto CAMEvent**](camevent.md) en el *parámetro pEvent* si la aplicación lo requiere. Debe establecer este evento después de procesar el evento mediante una expresión como:


```C++
pEvent->SetEvent
```



Se debe reservar un código de solicitud para que el subproceso de trabajo se cierre. Al recibir esta solicitud, devuelva 1 de esta función miembro. Devuelve 0 si no quieres que se cierre el subproceso de trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




