---
description: 'El método NewSegment notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento. Este método implementa el método IPin:: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Método CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680532"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="b29e6-104">CTransformInputPin. NewSegment, método</span><span class="sxs-lookup"><span data-stu-id="b29e6-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="b29e6-105">El `NewSegment` método notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento.</span><span class="sxs-lookup"><span data-stu-id="b29e6-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="b29e6-106">Este método implementa el método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="b29e6-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b29e6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b29e6-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="b29e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b29e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b29e6-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="b29e6-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e6-110">Hora de inicio del segmento.</span><span class="sxs-lookup"><span data-stu-id="b29e6-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="b29e6-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="b29e6-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e6-112">Hora de detención del segmento.</span><span class="sxs-lookup"><span data-stu-id="b29e6-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="b29e6-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="b29e6-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e6-114">Velocidad del segmento.</span><span class="sxs-lookup"><span data-stu-id="b29e6-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b29e6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b29e6-115">Return value</span></span>

<span data-ttu-id="b29e6-116">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b29e6-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b29e6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b29e6-117">Remarks</span></span>

<span data-ttu-id="b29e6-118">Este método invalida el método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="b29e6-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="b29e6-119">Llama al método [**CTransformFilter:: NewSegment**](ctransformfilter-newsegment.md) del filtro para proporcionar la llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b29e6-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29e6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b29e6-120">Requirements</span></span>



| <span data-ttu-id="b29e6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b29e6-121">Requirement</span></span> | <span data-ttu-id="b29e6-122">Value</span><span class="sxs-lookup"><span data-stu-id="b29e6-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b29e6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b29e6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b29e6-124"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b29e6-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b29e6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b29e6-125">Library</span></span><br/> | <dl> <span data-ttu-id="b29e6-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b29e6-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




