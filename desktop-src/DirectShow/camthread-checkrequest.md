---
description: El método CheckRequest comprueba si hay una solicitud, sin bloqueo.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Método CAMThread.CheckRequest (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662361"
---
# <a name="camthreadcheckrequest-method"></a>Método CAMThread.CheckRequest

El `CheckRequest` método comprueba si hay una solicitud, sin bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParam* 
</dt> <dd>

Puntero a una variable que recibe el valor pasado en la última llamada al [**método CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si hay una solicitud pendiente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método es una versión sin bloqueo del [**método CAMThread::GetRequest.**](camthread-getrequest.md)

Si otro subproceso está esperando una llamada a CallWorker, este método recupera el parámetro de solicitud y devuelve **TRUE**. De lo contrario, devuelve **FALSE.** Si el método devuelve **TRUE,** llame al [**método CAMThread::Reply**](camthread-reply.md) para liberar el subproceso solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




