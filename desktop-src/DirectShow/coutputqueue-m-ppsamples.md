---
description: 'Matriz de ejemplos de tamaño COutputQueue:: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Miembro COutputQueue:: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671097"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="57bf6-103">Miembro ppSamples COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="57bf6-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="57bf6-104">Matriz de ejemplos de tamaño [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="57bf6-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="57bf6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57bf6-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="57bf6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57bf6-106">Remarks</span></span>

<span data-ttu-id="57bf6-107">El subproceso de trabajo extrae ejemplos de la cola y los coloca en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="57bf6-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="57bf6-108">Pasa la matriz al método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="57bf6-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="57bf6-109">Si el objeto no utiliza un subproceso de trabajo, el objeto coloca ejemplos directamente en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="57bf6-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="57bf6-110">La variable miembro de [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) contiene la cola.</span><span class="sxs-lookup"><span data-stu-id="57bf6-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="57bf6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57bf6-111">Requirements</span></span>



| <span data-ttu-id="57bf6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="57bf6-112">Requirement</span></span> | <span data-ttu-id="57bf6-113">Value</span><span class="sxs-lookup"><span data-stu-id="57bf6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57bf6-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57bf6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="57bf6-115"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57bf6-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57bf6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57bf6-116">Library</span></span><br/> | <dl> <span data-ttu-id="57bf6-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="57bf6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57bf6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="57bf6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bf6-119">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="57bf6-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




