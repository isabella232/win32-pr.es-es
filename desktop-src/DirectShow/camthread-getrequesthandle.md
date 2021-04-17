---
description: 'El método GetRequestHandle recupera un identificador para el evento señalado por el método CAMThread:: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Método CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690732"
---
# <a name="camthreadgetrequesthandle-method"></a>CAMThread. GetRequestHandle, método

El `GetRequestHandle` método recupera un identificador para el evento señalado por el método [**CAMThread:: CallWorker**](camthread-callworker.md) .

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador de evento.

## <a name="remarks"></a>Observaciones

La clase CAMEvent mantiene un evento privado de restablecimiento manual, establecido por CallWorker y restablecido por el método [**CAMThread:: reply**](camthread-reply.md) .

Si llama a una función como WaitForMultipleObjects, use GetRequestHandle para recuperar el identificador de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




