---
description: 'El método Run ejecuta el filtro. Este método implementa el método IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660435"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="6dd51-104">CBaseFilter. Run (método)</span><span class="sxs-lookup"><span data-stu-id="6dd51-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="6dd51-105">El `Run` método ejecuta el filtro.</span><span class="sxs-lookup"><span data-stu-id="6dd51-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="6dd51-106">Este método implementa el método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="6dd51-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd51-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dd51-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="6dd51-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6dd51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd51-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="6dd51-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd51-110">Hora de referencia correspondiente al tiempo de secuencia 0.</span><span class="sxs-lookup"><span data-stu-id="6dd51-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd51-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dd51-111">Return value</span></span>

<span data-ttu-id="6dd51-112">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="6dd51-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd51-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6dd51-113">Remarks</span></span>

<span data-ttu-id="6dd51-114">Si se detiene el filtro, este método pausa el filtro llamando al método [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="6dd51-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="6dd51-115">A continuación, llama al método [**CBasePin:: Run**](cbasepin-run.md) en cada una de las clavijas conectadas del filtro.</span><span class="sxs-lookup"><span data-stu-id="6dd51-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="6dd51-116">Por último, establece la variable miembro de [**\_ Estado CBaseFilter:: m**](cbasefilter-m-state.md) en el estado en \_ ejecución.</span><span class="sxs-lookup"><span data-stu-id="6dd51-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="6dd51-117">El tiempo de secuencia se calcula como el tiempo de referencia actual menos *tStart*.</span><span class="sxs-lookup"><span data-stu-id="6dd51-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="6dd51-118">Un ejemplo multimedia con una marca de tiempo de cero se debe representar a la hora *tStart*.</span><span class="sxs-lookup"><span data-stu-id="6dd51-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd51-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dd51-119">Requirements</span></span>



| <span data-ttu-id="6dd51-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd51-120">Requirement</span></span> | <span data-ttu-id="6dd51-121">Value</span><span class="sxs-lookup"><span data-stu-id="6dd51-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd51-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6dd51-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6dd51-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd51-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6dd51-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6dd51-124">Library</span></span><br/> | <dl> <span data-ttu-id="6dd51-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd51-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dd51-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dd51-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd51-127">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6dd51-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




