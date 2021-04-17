---
description: El método NewSegment entrega un nuevo segmento al pin de entrada.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Método COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680476"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="f2831-103">COutputQueue. NewSegment, método</span><span class="sxs-lookup"><span data-stu-id="f2831-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="f2831-104">El `NewSegment` método entrega un nuevo segmento al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="f2831-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2831-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2831-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="f2831-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2831-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="f2831-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f2831-108">Posición del medio inicial del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f2831-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f2831-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="f2831-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f2831-110">Fin de la posición del medio del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f2831-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f2831-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="f2831-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f2831-112">Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.</span><span class="sxs-lookup"><span data-stu-id="f2831-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2831-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2831-113">Return value</span></span>

<span data-ttu-id="f2831-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2831-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2831-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2831-115">Remarks</span></span>

<span data-ttu-id="f2831-116">Si el objeto utiliza un subproceso, pone en cola los elementos siguientes, en orden:</span><span class="sxs-lookup"><span data-stu-id="f2831-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="f2831-117">NUEVO \_ mensaje de control de segmento.</span><span class="sxs-lookup"><span data-stu-id="f2831-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="f2831-118">Datos del segmento.</span><span class="sxs-lookup"><span data-stu-id="f2831-118">The segment data.</span></span>

<span data-ttu-id="f2831-119">El nuevo \_ mensaje de segmento notifica al subproceso que el siguiente elemento de la cola contendrá datos de segmento.</span><span class="sxs-lookup"><span data-stu-id="f2831-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="f2831-120">Los datos del segmento se agrupan en una estructura, que se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f2831-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="f2831-121">El subproceso llama al método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el PIN de entrada, con los datos especificados en la estructura.</span><span class="sxs-lookup"><span data-stu-id="f2831-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="f2831-122">Si el objeto no utiliza un subproceso, llama al método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para proporcionar cualquier ejemplo pendiente.</span><span class="sxs-lookup"><span data-stu-id="f2831-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="f2831-123">A continuación, llama a **IPin:: NewSegment** en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="f2831-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2831-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2831-124">Requirements</span></span>



| <span data-ttu-id="f2831-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2831-125">Requirement</span></span> | <span data-ttu-id="f2831-126">Value</span><span class="sxs-lookup"><span data-stu-id="f2831-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2831-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2831-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f2831-128"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2831-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2831-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2831-129">Library</span></span><br/> | <dl> <span data-ttu-id="f2831-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f2831-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2831-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2831-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2831-132">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="f2831-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




