---
description: El método CheckRequest comprueba si hay una solicitud, sin bloqueos.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Método CAMThread. CheckRequest (Wxutil. h)
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
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690444"
---
# <a name="camthreadcheckrequest-method"></a>CAMThread. CheckRequest, método

El `CheckRequest` método comprueba si hay una solicitud, sin bloqueos.

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

Puntero a una variable que recibe el valor pasado en la última llamada al método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si hay una solicitud pendiente o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método es una versión que no es de bloqueo del método [**CAMThread:: GetRequest**](camthread-getrequest.md) .

Si otro subproceso está esperando en una llamada a CallWorker, este método recupera el parámetro de solicitud y devuelve **true**. De lo contrario, devuelve **false**. Si el método devuelve **true**, llame al método [**CAMThread:: reply**](camthread-reply.md) para liberar el subproceso que lo solicita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




