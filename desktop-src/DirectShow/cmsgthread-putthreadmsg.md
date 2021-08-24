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
ms.openlocfilehash: 7eefa95c4fd6ab19c895b4d1d47dba3a19302023985a4631708c3cf7ccc10d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585645"
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

## <a name="remarks"></a>Comentarios

Esta función miembro pone en cola una solicitud de ejecución por parte del subproceso de trabajo. Los parámetros de esta función miembro se pondrán en cola (en un objeto [**CMsg)**](cmsg.md) y se pasarán a la función miembro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) del subproceso de trabajo. Esta función miembro devuelve inmediatamente después de hacer cola la solicitud y no espera a que el subproceso cumpla la solicitud. La **función miembro CMsgThread::ThreadMessageProc** de la clase derivada define los cuatro parámetros.

Esta función miembro usa una lista segura para multiproceso, por lo que se pueden realizar varias llamadas a esta función miembro desde distintos subprocesos de forma segura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




