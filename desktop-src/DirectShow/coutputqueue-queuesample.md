---
description: El método QueueSample pone en cola un ejemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue. QueueSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678977"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="74096-103">COutputQueue. QueueSample, método</span><span class="sxs-lookup"><span data-stu-id="74096-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="74096-104">El `QueueSample` método pone en cola un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="74096-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="74096-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74096-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="74096-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74096-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74096-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="74096-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="74096-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="74096-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74096-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74096-109">Return value</span></span>

<span data-ttu-id="74096-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="74096-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74096-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74096-111">Remarks</span></span>

<span data-ttu-id="74096-112">Este método agrega un ejemplo al final de la cola.</span><span class="sxs-lookup"><span data-stu-id="74096-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="74096-113">Mantenga la sección crítica antes de llamar a este método y llámela solo cuando el objeto esté utilizando un subproceso para ofrecer ejemplos.</span><span class="sxs-lookup"><span data-stu-id="74096-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="74096-114">Para determinar si el objeto está utilizando un subproceso, llame al método [**COutputQueue:: IsQueued**](coutputqueue-isqueued.md) .</span><span class="sxs-lookup"><span data-stu-id="74096-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="74096-115">Este método también se puede utilizar para colocar mensajes de control en la cola.</span><span class="sxs-lookup"><span data-stu-id="74096-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="74096-116">Un mensaje de control es una constante definida (convertida en un \_ tipo Long PTR) que indica al subproceso que realice alguna acción.</span><span class="sxs-lookup"><span data-stu-id="74096-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="74096-117">La clase **COutputQueue** define los mensajes de control que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="74096-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="74096-118">Message</span><span class="sxs-lookup"><span data-stu-id="74096-118">Message</span></span>       | <span data-ttu-id="74096-119">Acción</span><span class="sxs-lookup"><span data-stu-id="74096-119">Action</span></span>                                 |
| <span data-ttu-id="74096-120">paquete de EOS \_</span><span class="sxs-lookup"><span data-stu-id="74096-120">EOS\_PACKET</span></span>   | <span data-ttu-id="74096-121">Entrega de una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="74096-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="74096-122">NUEVO \_ segmento</span><span class="sxs-lookup"><span data-stu-id="74096-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="74096-123">Entregue un nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="74096-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="74096-124">RESTABLECER \_ paquete</span><span class="sxs-lookup"><span data-stu-id="74096-124">RESET\_PACKET</span></span> | <span data-ttu-id="74096-125">Restablecer el estado de la cola.</span><span class="sxs-lookup"><span data-stu-id="74096-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="74096-126">ENVIAR \_ paquete</span><span class="sxs-lookup"><span data-stu-id="74096-126">SEND\_PACKET</span></span>  | <span data-ttu-id="74096-127">Enviar un lote parcial de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="74096-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="74096-128">Se trata de un método protegido, que la clase **COutputQueue** usa internamente.</span><span class="sxs-lookup"><span data-stu-id="74096-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="74096-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74096-129">Requirements</span></span>



| <span data-ttu-id="74096-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="74096-130">Requirement</span></span> | <span data-ttu-id="74096-131">Value</span><span class="sxs-lookup"><span data-stu-id="74096-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74096-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74096-132">Header</span></span><br/>  | <dl> <span data-ttu-id="74096-133"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74096-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74096-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74096-134">Library</span></span><br/> | <dl> <span data-ttu-id="74096-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="74096-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74096-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="74096-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74096-137">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="74096-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




