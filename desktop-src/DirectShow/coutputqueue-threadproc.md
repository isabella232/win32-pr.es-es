---
description: El método ThreadProc recupera ejemplos de la cola y los entrega al pin de entrada.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Método COutputQueue. ThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670405"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="3ac47-103">COutputQueue. ThreadProc (método)</span><span class="sxs-lookup"><span data-stu-id="3ac47-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="3ac47-104">El `ThreadProc` método recupera ejemplos de la cola y los entrega al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="3ac47-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ac47-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="3ac47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ac47-106">Parameters</span></span>

<span data-ttu-id="3ac47-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3ac47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ac47-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac47-108">Return value</span></span>

<span data-ttu-id="3ac47-109">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3ac47-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac47-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ac47-110">Remarks</span></span>

<span data-ttu-id="3ac47-111">El método [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) llama a este método, que implementa el bucle de subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="3ac47-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="3ac47-112">Dentro del bucle, el método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3ac47-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="3ac47-113">Recupera un ejemplo para la cola.</span><span class="sxs-lookup"><span data-stu-id="3ac47-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="3ac47-114">Si el ejemplo es un mensaje de control, el subproceso ejecuta la acción de control.</span><span class="sxs-lookup"><span data-stu-id="3ac47-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="3ac47-115">De lo contrario, coloca el ejemplo en la matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac47-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="3ac47-116">Cuando la matriz está llena (o si [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) es **false**), el subproceso llama al método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) para proporcionar los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3ac47-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="3ac47-117">Si no hay ningún ejemplo en cola, el subproceso espera en el semáforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac47-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="3ac47-118">El subproceso finaliza cuando la variable miembro [**COutputQueue:: m \_ BTerminate**](coutputqueue-m-bterminate.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="3ac47-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac47-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac47-119">Requirements</span></span>



| <span data-ttu-id="3ac47-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac47-120">Requirement</span></span> | <span data-ttu-id="3ac47-121">Value</span><span class="sxs-lookup"><span data-stu-id="3ac47-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac47-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ac47-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3ac47-123"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac47-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ac47-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ac47-124">Library</span></span><br/> | <dl> <span data-ttu-id="3ac47-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac47-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac47-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ac47-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac47-127">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="3ac47-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




