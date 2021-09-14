---
description: El método GetRequest espera la siguiente solicitud.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Método CAMThread.GetRequest (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160254"
---
# <a name="camthreadgetrequest-method"></a>Método CAMThread.GetRequest

El `GetRequest` método espera a la siguiente solicitud.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor definido por la clase derivada.

## <a name="remarks"></a>Observaciones

Este método se bloquea hasta que otro subproceso llama [**al método CAMThread::CallWorker.**](camthread-callworker.md) A continuación, devuelve el parámetro que se pasó a CallWorker. Llame al [**método CAMThread::Reply**](camthread-reply.md) para liberar el subproceso solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




