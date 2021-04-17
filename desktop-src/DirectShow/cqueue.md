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
# <a name="cqueue-class"></a><span data-ttu-id="b4e87-103">Clase CQueue</span><span class="sxs-lookup"><span data-stu-id="b4e87-103">CQueue class</span></span>

<span data-ttu-id="b4e87-104">La plantilla de clase **CQueue** implementa una cola sencilla y de tamaño estático.</span><span class="sxs-lookup"><span data-stu-id="b4e87-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="b4e87-105">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="b4e87-105">Public Methods</span></span>                                  | <span data-ttu-id="b4e87-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4e87-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="b4e87-107">**CQueue**</span><span class="sxs-lookup"><span data-stu-id="b4e87-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="b4e87-108">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="b4e87-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="b4e87-109">**~ CQueue**</span><span class="sxs-lookup"><span data-stu-id="b4e87-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="b4e87-110">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="b4e87-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="b4e87-111">**GetQueueObject**</span><span class="sxs-lookup"><span data-stu-id="b4e87-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="b4e87-112">Recupera el siguiente elemento de la cola.</span><span class="sxs-lookup"><span data-stu-id="b4e87-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="b4e87-113">**PutQueueObject**</span><span class="sxs-lookup"><span data-stu-id="b4e87-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="b4e87-114">Coloca un elemento en la cola.</span><span class="sxs-lookup"><span data-stu-id="b4e87-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b4e87-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4e87-115">Remarks</span></span>

<span data-ttu-id="b4e87-116">El constructor de clase especifica el tamaño de la cola.</span><span class="sxs-lookup"><span data-stu-id="b4e87-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="b4e87-117">Use [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) para colocar un elemento en la cola y el método [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) para quitar de la cola un elemento.</span><span class="sxs-lookup"><span data-stu-id="b4e87-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="b4e87-118">Si la cola está llena, el método **PutQueueObject** se bloquea hasta que se quita un elemento de la cola.</span><span class="sxs-lookup"><span data-stu-id="b4e87-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="b4e87-119">Si la cola está vacía, el **GetQueueObject** se bloquea hasta que un elemento se pone en cola.</span><span class="sxs-lookup"><span data-stu-id="b4e87-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="b4e87-120">El parámetro de plantilla especifica el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="b4e87-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="b4e87-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b4e87-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="b4e87-122">La clase utiliza dos semáforos para controlar las operaciones de cola, un semáforo "Get" y un semáforo "put".</span><span class="sxs-lookup"><span data-stu-id="b4e87-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="b4e87-123">El método [**GetQueueObject**](cqueue-getqueueobject.md) espera en el semáforo "Get" (mediante la función **WaitForSingleObject** ) y libera el semáforo "put" (mediante la función **ReleaseSemaphore (** ).</span><span class="sxs-lookup"><span data-stu-id="b4e87-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="b4e87-124">El método [**PutQueueObject**](cqueue-putqueueobject.md) espera en el semáforo "put" y suelta el semáforo "Get".</span><span class="sxs-lookup"><span data-stu-id="b4e87-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="b4e87-125">La clase usa una sección crítica para serializar las operaciones de cola entre varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b4e87-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e87-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4e87-126">Requirements</span></span>



| <span data-ttu-id="b4e87-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4e87-127">Requirement</span></span> | <span data-ttu-id="b4e87-128">Value</span><span class="sxs-lookup"><span data-stu-id="b4e87-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e87-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4e87-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b4e87-130"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4e87-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b4e87-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4e87-131">Library</span></span><br/> | <dl> <span data-ttu-id="b4e87-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b4e87-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




