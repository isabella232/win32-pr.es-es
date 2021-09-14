---
description: Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Método CMsgThread.PutThreadMsg (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973863"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Método CMsgThread.PutThreadMsg

Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.

## <a name="syntax"></a>Sintaxis


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Código de solicitud.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Parámetro flags opcional.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Puntero opcional a un bloque de datos que contiene parámetros adicionales o valores devueltos. Debe ser estático o asignado al montón y no automático.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntero opcional a un objeto de evento que se va a señalar tras la finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro pone en cola una solicitud de ejecución por parte del subproceso de trabajo. Los parámetros de esta función miembro se pondrán en cola (en un objeto [**CMsg)**](cmsg.md) y se pasarán a la función miembro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) del subproceso de trabajo. Esta función miembro devuelve inmediatamente después de hacer cola la solicitud y no espera a que el subproceso cumpla la solicitud. La **función miembro CMsgThread::ThreadMessageProc** de la clase derivada define los cuatro parámetros.

Esta función miembro usa una lista segura para multiproceso, por lo que se pueden realizar varias llamadas a esta función miembro desde distintos subprocesos de forma segura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




