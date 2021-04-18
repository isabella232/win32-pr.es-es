---
description: El método WaitForRenderTime espera el tiempo de presentación del ejemplo actual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660134"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="b169c-103">CBaseRenderer. WaitForRenderTime, método</span><span class="sxs-lookup"><span data-stu-id="b169c-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="b169c-104">El `WaitForRenderTime` método espera el tiempo de presentación del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="b169c-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b169c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b169c-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="b169c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b169c-106">Parameters</span></span>

<span data-ttu-id="b169c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b169c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b169c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b169c-108">Return value</span></span>

<span data-ttu-id="b169c-109">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b169c-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="b169c-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b169c-110">Return code</span></span>                                                                                           | <span data-ttu-id="b169c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b169c-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b169c-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b169c-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="b169c-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b169c-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b169c-114"><dt>**Estado de VFW \_ E \_ \_ cambiado**</dt></span><span class="sxs-lookup"><span data-stu-id="b169c-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="b169c-115">El estado del filtro cambió antes de que llegara el tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="b169c-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b169c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b169c-116">Remarks</span></span>

<span data-ttu-id="b169c-117">Este método espera hasta que se produce uno de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="b169c-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="b169c-118">Llega el tiempo de presentación del ejemplo, en el que se puede representar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b169c-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="b169c-119">El filtro detiene o inicia el vaciado de datos.</span><span class="sxs-lookup"><span data-stu-id="b169c-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="b169c-120">Si llega el momento de la presentación, se señala el evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b169c-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="b169c-121">Si el estado cambia, se señala el evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) .</span><span class="sxs-lookup"><span data-stu-id="b169c-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="b169c-122">Este método espera en ambos eventos.</span><span class="sxs-lookup"><span data-stu-id="b169c-122">This method waits on both events.</span></span> <span data-ttu-id="b169c-123">La clase derivada puede invalidar este método para esperar en eventos adicionales, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b169c-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="b169c-124">Este método llama al método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) cuando comienza la espera y el método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) cuando se realiza la espera.</span><span class="sxs-lookup"><span data-stu-id="b169c-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="b169c-125">Ninguno de los métodos realiza ninguna acción en la clase base, pero la clase derivada puede invalidarlos.</span><span class="sxs-lookup"><span data-stu-id="b169c-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="b169c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b169c-126">Requirements</span></span>



| <span data-ttu-id="b169c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b169c-127">Requirement</span></span> | <span data-ttu-id="b169c-128">Value</span><span class="sxs-lookup"><span data-stu-id="b169c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b169c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b169c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b169c-130"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b169c-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b169c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b169c-131">Library</span></span><br/> | <dl> <span data-ttu-id="b169c-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b169c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b169c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b169c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b169c-134">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b169c-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




