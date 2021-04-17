---
description: La plantilla de clase CQueue implementa una cola sencilla y de tamaño estático.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Clase CQueue (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680863"
---
# <a name="cqueue-class"></a>Clase CQueue

La plantilla de clase **CQueue** implementa una cola sencilla y de tamaño estático.



| Métodos públicos                                  | Descripción                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Método de constructor.                     |
| [**~ CQueue**](cqueue--cqueue.md)               | Método de destructor.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Recupera el siguiente elemento de la cola. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Coloca un elemento en la cola.            |



 

## <a name="remarks"></a>Observaciones

El constructor de clase especifica el tamaño de la cola. Use [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) para colocar un elemento en la cola y el método [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) para quitar de la cola un elemento. Si la cola está llena, el método **PutQueueObject** se bloquea hasta que se quita un elemento de la cola. Si la cola está vacía, el **GetQueueObject** se bloquea hasta que un elemento se pone en cola. El parámetro de plantilla especifica el tipo de elemento. Por ejemplo:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



La clase utiliza dos semáforos para controlar las operaciones de cola, un semáforo "Get" y un semáforo "put". El método [**GetQueueObject**](cqueue-getqueueobject.md) espera en el semáforo "Get" (mediante la función **WaitForSingleObject** ) y libera el semáforo "put" (mediante la función **ReleaseSemaphore (** ). El método [**PutQueueObject**](cqueue-putqueueobject.md) espera en el semáforo "put" y suelta el semáforo "Get". La clase usa una sección crítica para serializar las operaciones de cola entre varios subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




