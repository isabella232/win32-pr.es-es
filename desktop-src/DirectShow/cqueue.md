---
description: La plantilla de clase CQueue implementa una cola sencilla de tamaño estático.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: CQueue (clase, Wxutil.h)
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
ms.openlocfilehash: bf6c6225a393f8f6ff1848acc66c68b6d260b0c839f2cc9f1e24d06a11e88219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953984"
---
# <a name="cqueue-class"></a>CQueue (clase)

La **plantilla de clase CQueue** implementa una cola sencilla de tamaño estático.



| Métodos públicos                                  | Descripción                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Método constructor.                     |
| [**~CQueue**](cqueue--cqueue.md)               | Método destructor.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Recupera el siguiente elemento de la cola. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Coloca un elemento en la cola.            |



 

## <a name="remarks"></a>Comentarios

El constructor de clase especifica el tamaño de la cola. Use [**CQueue::P utQueueObject**](cqueue-putqueueobject.md) para colocar un elemento en la cola y el método [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) para quitar la cola de un elemento. Si la cola está llena, el **método PutQueueObject** se bloquea hasta que se quita de la cola un elemento. Si la cola está vacía, **GetQueueObject** se bloquea hasta que se pone en cola un elemento. El parámetro de plantilla especifica el tipo de elemento. Por ejemplo:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



La clase usa dos semáforos para controlar las operaciones de puesta en cola, un semáforo "get" y un semáforo "put". El [**método GetQueueObject**](cqueue-getqueueobject.md) espera en el semáforo "get" (mediante la función **WaitForSingleObject)** y libera el semáforo "put" (mediante la **función ReleaseSemaphore).** El [**método PutQueueObject**](cqueue-putqueueobject.md) espera en el semáforo "put" y libera el semáforo "get". La clase usa una sección crítica para serializar las operaciones de cola entre varios subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




