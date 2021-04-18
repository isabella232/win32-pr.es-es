---
description: Recupera un objeto CMsg en cola que contiene una solicitud.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Método CMsgThread. GetThreadMsg (Msgthrd. h)
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
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680346"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>CMsgThread. GetThreadMsg, método

Recupera un objeto [**CMsg**](cmsg.md) en cola que contiene una solicitud.

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

## <a name="remarks"></a>Observaciones

Se llama a esta función miembro desde la función [**ThreadProc**](camthread-threadproc.md) Private del subproceso de trabajo para recuperar la función miembro siguiente. El parámetro *MSG* debe apuntar a un objeto [**CMsg**](cmsg.md) asignado que se rellenará con los parámetros de la siguiente solicitud de la cola. Si no hay ninguna solicitud en cola, esta función miembro se bloquea hasta que se pone en cola la siguiente solicitud (mediante una llamada a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




