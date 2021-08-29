---
description: Recupera un objeto CMsg en cola que contiene una solicitud.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Método CMsgThread.GetThreadMsg (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5badc43e2bcdebd5d251ce657f2ec61ae90ec9ea53f372634a4edeaf5cfc4db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831865"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>Método CMsgThread.GetThreadMsg

Recupera un objeto [**CMsg en**](cmsg.md) cola que contiene una solicitud.

## <a name="syntax"></a>Sintaxis


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*msg* 
</dt> <dd>

Puntero a un objeto [**CMsg**](cmsg.md) asignado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se llama a esta función miembro desde la función [**ThreadProc**](camthread-threadproc.md) privada del subproceso de trabajo para recuperar la siguiente función miembro. El *parámetro msg* debe apuntar a un objeto [**CMsg**](cmsg.md) asignado que se rellenará con los parámetros para la siguiente solicitud en la cola. Si no hay solicitudes en cola, esta función miembro se bloquea hasta que se pone en cola la siguiente solicitud (mediante una llamada a la función miembro [**CMsgThread::P utThreadMsg).**](cmsgthread-putthreadmsg.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




