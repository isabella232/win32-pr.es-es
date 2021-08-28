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
ms.openlocfilehash: f2527d43dfa59ab01bc57109bd2845e5da8286524612746067b1ff2f4cb2a3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103205"
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

## <a name="remarks"></a>Comentarios

Este método se bloquea hasta que otro subproceso llama [**al método CAMThread::CallWorker.**](camthread-callworker.md) A continuación, devuelve el parámetro que se pasó a CallWorker. Llame al [**método CAMThread::Reply**](camthread-reply.md) para liberar el subproceso solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




