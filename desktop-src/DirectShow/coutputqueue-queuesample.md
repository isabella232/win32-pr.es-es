---
description: El método QueueSample pone en cola un ejemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue.QueueSample (Outputq.h)
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
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910073"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="20fc5-103">Método COutputQueue.QueueSample</span><span class="sxs-lookup"><span data-stu-id="20fc5-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="20fc5-104">El `QueueSample` método pone en cola un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20fc5-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fc5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20fc5-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="20fc5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20fc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fc5-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="20fc5-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="20fc5-108">Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20fc5-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fc5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20fc5-109">Return value</span></span>

<span data-ttu-id="20fc5-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="20fc5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20fc5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20fc5-111">Remarks</span></span>

<span data-ttu-id="20fc5-112">Este método agrega un ejemplo al final de la cola.</span><span class="sxs-lookup"><span data-stu-id="20fc5-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="20fc5-113">Mantenga la sección crítica antes de llamar a este método y llámelo solo cuando el objeto use un subproceso para entregar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="20fc5-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="20fc5-114">Para determinar si el objeto usa un subproceso, llame al [**método COutputQueue::IsQueued.**](coutputqueue-isqueued.md)</span><span class="sxs-lookup"><span data-stu-id="20fc5-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="20fc5-115">Este método también se puede usar para colocar mensajes de control en la cola.</span><span class="sxs-lookup"><span data-stu-id="20fc5-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="20fc5-116">Un mensaje de control es una constante definida (conversión a un tipo LONG PTR) que indica al subproceso \_ que realice alguna acción.</span><span class="sxs-lookup"><span data-stu-id="20fc5-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="20fc5-117">La **clase COutputQueue** define los mensajes de control que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="20fc5-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="20fc5-118">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="20fc5-118">Label</span></span> | <span data-ttu-id="20fc5-119">Value</span><span class="sxs-lookup"><span data-stu-id="20fc5-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="20fc5-120">Message</span><span class="sxs-lookup"><span data-stu-id="20fc5-120">Message</span></span>       | <span data-ttu-id="20fc5-121">Acción</span><span class="sxs-lookup"><span data-stu-id="20fc5-121">Action</span></span>                                 |
| <span data-ttu-id="20fc5-122">PAQUETE \_ EOS</span><span class="sxs-lookup"><span data-stu-id="20fc5-122">EOS\_PACKET</span></span>   | <span data-ttu-id="20fc5-123">Entrega de una notificación de fin de flujo.</span><span class="sxs-lookup"><span data-stu-id="20fc5-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="20fc5-124">NUEVO \_ SEGMENTO</span><span class="sxs-lookup"><span data-stu-id="20fc5-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="20fc5-125">Entrega de un nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="20fc5-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="20fc5-126">RESTABLECER \_ PAQUETE</span><span class="sxs-lookup"><span data-stu-id="20fc5-126">RESET\_PACKET</span></span> | <span data-ttu-id="20fc5-127">Restablezca el estado de la cola.</span><span class="sxs-lookup"><span data-stu-id="20fc5-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="20fc5-128">ENVÍO DE \_ PAQUETES</span><span class="sxs-lookup"><span data-stu-id="20fc5-128">SEND\_PACKET</span></span>  | <span data-ttu-id="20fc5-129">Envíe un lote parcial de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="20fc5-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="20fc5-130">Se trata de un método protegido que la **clase COutputQueue** usa internamente.</span><span class="sxs-lookup"><span data-stu-id="20fc5-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="20fc5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fc5-131">Requirements</span></span>



| <span data-ttu-id="20fc5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fc5-132">Requirement</span></span> | <span data-ttu-id="20fc5-133">Value</span><span class="sxs-lookup"><span data-stu-id="20fc5-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fc5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20fc5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="20fc5-135"><dt>Outputq.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fc5-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20fc5-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20fc5-136">Library</span></span><br/> | <dl> <span data-ttu-id="20fc5-137"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="20fc5-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fc5-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20fc5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fc5-139">**COutputQueue (clase)**</span><span class="sxs-lookup"><span data-stu-id="20fc5-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




