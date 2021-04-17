---
description: Procesa las solicitudes. Se trata de una función miembro virtual pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Método CMsgThread. ThreadMessageProc (Msgthrd. h)
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
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671221"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>CMsgThread. ThreadMessageProc, método

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

Parámetro opcional de la marca que se va a solicitar.

</dd> <dt>

*lpParam* 
</dt> <dd>

Puntero opcional a datos adicionales o un bloque de datos devuelto.

</dd> <dt>

*As* 
</dt> <dd>

Puntero opcional a un objeto de evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cualquier devolución distinto de cero hace que el subproceso se cierre. Devuelve cero a menos que se haya procesado recientemente una solicitud de salida.

## <a name="remarks"></a>Observaciones

Esta función virtual pura se debe invalidar en la clase derivada. Se llamará una vez para cada solicitud puesta en cola mediante una llamada a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .

La función miembro define los cuatro parámetros. Normalmente, use el parámetro *uMsg* para indicar la solicitud y los otros tres parámetros serán parámetros adicionales opcionales. La aplicación que realiza la llamada puede proporcionar un puntero a un objeto [**CAMEvent**](camevent.md) en el parámetro *pevent* si la aplicación lo requiere. Debe establecer este evento después de procesar el evento mediante una expresión como:


```C++
pEvent->SetEvent
```



Se debe reservar un código de solicitud para indicar al subproceso de trabajo que se cierre. Al recibir esta solicitud, devuelve 1 de esta función miembro. Devuelve 0 si no desea que el subproceso de trabajo salga.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




