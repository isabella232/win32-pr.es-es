---
description: 'Método COutputQueue.EndFlush: el método EndFlush finaliza una operación de vaciado.'
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue.EndFlush (Outputq.h)
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
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099013"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="9a1bd-103">Método COutputQueue.EndFlush</span><span class="sxs-lookup"><span data-stu-id="9a1bd-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="9a1bd-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="9a1bd-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a1bd-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="9a1bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a1bd-106">Parameters</span></span>

<span data-ttu-id="9a1bd-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a1bd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a1bd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a1bd-108">Return value</span></span>

<span data-ttu-id="9a1bd-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9a1bd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1bd-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a1bd-110">Remarks</span></span>

<span data-ttu-id="9a1bd-111">Si el objeto usa un subproceso, este método espera el evento [**COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="9a1bd-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="9a1bd-112">El subproceso señala este evento después de liberar los ejemplos pendientes.</span><span class="sxs-lookup"><span data-stu-id="9a1bd-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="9a1bd-113">Si el objeto no usa un subproceso, este método llama al [**método COutputQueue::FreeSamples.**](coutputqueue-freesamples.md)</span><span class="sxs-lookup"><span data-stu-id="9a1bd-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="9a1bd-114">A `EndFlush` continuación, el método [**llama al método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="9a1bd-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1bd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a1bd-115">Requirements</span></span>



| <span data-ttu-id="9a1bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a1bd-116">Requirement</span></span> | <span data-ttu-id="9a1bd-117">Value</span><span class="sxs-lookup"><span data-stu-id="9a1bd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1bd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a1bd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9a1bd-119"><dt>Outputq.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a1bd-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a1bd-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a1bd-120">Library</span></span><br/> | <dl> <span data-ttu-id="9a1bd-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9a1bd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a1bd-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9a1bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1bd-123">**COutputQueue (clase)**</span><span class="sxs-lookup"><span data-stu-id="9a1bd-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




