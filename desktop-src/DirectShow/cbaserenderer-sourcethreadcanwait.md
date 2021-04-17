---
description: El método SourceThreadCanWait contiene o libera el subproceso de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661269"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="185e4-103">CBaseRenderer. SourceThreadCanWait, método</span><span class="sxs-lookup"><span data-stu-id="185e4-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="185e4-104">El `SourceThreadCanWait` método contiene o libera el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="185e4-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="185e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="185e4-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="185e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="185e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="185e4-107">*bCanWait*</span><span class="sxs-lookup"><span data-stu-id="185e4-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="185e4-108">Valor booleano que indica si se va a contener el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="185e4-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="185e4-109">Si es **true**, se bloquea el subproceso de streaming mientras el filtro espera a representar los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="185e4-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="185e4-110">Si es **false**, se libera el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="185e4-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="185e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="185e4-111">Return value</span></span>

<span data-ttu-id="185e4-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="185e4-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="185e4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="185e4-113">Remarks</span></span>

<span data-ttu-id="185e4-114">Al llamar al `SourceThreadCanWait` método con el valor **false** , el filtro se devuelve de una llamada a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada.</span><span class="sxs-lookup"><span data-stu-id="185e4-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="185e4-115">Cuando el filtro se está ejecutando, bloquea las llamadas de **recepción** hasta el momento de la presentación del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="185e4-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="185e4-116">Cuando el filtro está en pausa, bloquea las llamadas de **recepción** indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="185e4-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="185e4-117">Este comportamiento regula el flujo de datos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="185e4-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="185e4-118">Sin embargo, cuando el filtro se detiene o se vuelca, no debería bloquearse.</span><span class="sxs-lookup"><span data-stu-id="185e4-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="185e4-119">El bloqueo se controla mediante el método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , que espera dos eventos: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) y [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="185e4-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="185e4-120">El evento **m \_ RenderEvent** se señala cuando llega el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="185e4-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="185e4-121">El evento **m \_ ThreadSignal** se señaliza cuando `SourceThreadCanWait` se llama a con el valor **false**.</span><span class="sxs-lookup"><span data-stu-id="185e4-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="185e4-122">Al llamar a `SourceThreadCanWait` con el valor **true** , se restablece el evento.</span><span class="sxs-lookup"><span data-stu-id="185e4-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="185e4-123">Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a `SourceThreadCanWait` con el valor **false** (liberando el subproceso de streaming).</span><span class="sxs-lookup"><span data-stu-id="185e4-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="185e4-124">Los métodos [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)y [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) llaman a `SourceThreadCanWait` con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="185e4-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="185e4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="185e4-125">Requirements</span></span>



| <span data-ttu-id="185e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="185e4-126">Requirement</span></span> | <span data-ttu-id="185e4-127">Value</span><span class="sxs-lookup"><span data-stu-id="185e4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="185e4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="185e4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="185e4-129"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="185e4-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="185e4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="185e4-130">Library</span></span><br/> | <dl> <span data-ttu-id="185e4-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="185e4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185e4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="185e4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185e4-133">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="185e4-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




