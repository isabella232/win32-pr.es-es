---
description: El método GetRequest espera a la solicitud siguiente.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Método CAMThread. GetRequest (Wxutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690576"
---
# <a name="camthreadgetrequest-method"></a>CAMThread. GetRequest, método

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

Este método se bloquea hasta que otro subproceso llama al método [**CAMThread:: CallWorker**](camthread-callworker.md) . A continuación, devuelve el parámetro que se pasó a CallWorker. Llame al método [**CAMThread:: reply**](camthread-reply.md) para liberar el subproceso que lo solicita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




