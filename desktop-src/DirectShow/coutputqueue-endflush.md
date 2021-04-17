---
description: El método EndFlush finaliza una operación de vaciado.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671215"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="1dbdd-103">COutputQueue. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="1dbdd-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="1dbdd-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dbdd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dbdd-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1dbdd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dbdd-106">Parameters</span></span>

<span data-ttu-id="1dbdd-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1dbdd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dbdd-108">Return value</span></span>

<span data-ttu-id="1dbdd-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dbdd-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dbdd-110">Remarks</span></span>

<span data-ttu-id="1dbdd-111">Si el objeto utiliza un subproceso, este método espera el evento [**COutputQueue:: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="1dbdd-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="1dbdd-112">El subproceso señala este evento después de liberar cualquier ejemplo pendiente.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="1dbdd-113">Si el objeto no utiliza un subproceso, este método llama al método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) .</span><span class="sxs-lookup"><span data-stu-id="1dbdd-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="1dbdd-114">Después, el `EndFlush` método llama al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dbdd-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dbdd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dbdd-115">Requirements</span></span>



| <span data-ttu-id="1dbdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dbdd-116">Requirement</span></span> | <span data-ttu-id="1dbdd-117">Value</span><span class="sxs-lookup"><span data-stu-id="1dbdd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbdd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dbdd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1dbdd-119"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dbdd-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1dbdd-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dbdd-120">Library</span></span><br/> | <dl> <span data-ttu-id="1dbdd-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1dbdd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dbdd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dbdd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbdd-123">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="1dbdd-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




