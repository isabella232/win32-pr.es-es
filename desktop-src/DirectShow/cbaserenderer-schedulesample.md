---
description: El método ScheduleSample programa un ejemplo para la representación.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661137"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="2117a-103">CBaseRenderer. ScheduleSample, método</span><span class="sxs-lookup"><span data-stu-id="2117a-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="2117a-104">El `ScheduleSample` método programa un ejemplo para la representación.</span><span class="sxs-lookup"><span data-stu-id="2117a-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="2117a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2117a-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="2117a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2117a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2117a-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="2117a-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2117a-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2117a-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2117a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2117a-109">Return value</span></span>

<span data-ttu-id="2117a-110">Devuelve **true** si se ha programado el ejemplo, o **false** si se ha quitado el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2117a-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="2117a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2117a-111">Remarks</span></span>

<span data-ttu-id="2117a-112">En primer lugar, este método determina si el ejemplo se debe representar inmediatamente, se representa en el futuro o se quita.</span><span class="sxs-lookup"><span data-stu-id="2117a-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="2117a-113">(Para ello, llama al método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) ). Si el ejemplo se debe representar inmediatamente, el método señala al evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="2117a-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="2117a-114">Si el ejemplo se debe representar en el futuro, el método llama al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para la programación.</span><span class="sxs-lookup"><span data-stu-id="2117a-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="2117a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2117a-115">Requirements</span></span>



| <span data-ttu-id="2117a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2117a-116">Requirement</span></span> | <span data-ttu-id="2117a-117">Value</span><span class="sxs-lookup"><span data-stu-id="2117a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2117a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2117a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2117a-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2117a-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2117a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2117a-120">Library</span></span><br/> | <dl> <span data-ttu-id="2117a-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2117a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2117a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2117a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2117a-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2117a-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




