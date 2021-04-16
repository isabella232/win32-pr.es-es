---
description: El método PAUSE pausa el filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Método CBaseRenderer. PAUSE (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671734"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="2f42a-103">CBaseRenderer. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="2f42a-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="2f42a-104">El `Pause` método pausa el filtro.</span><span class="sxs-lookup"><span data-stu-id="2f42a-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f42a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f42a-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="2f42a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f42a-106">Parameters</span></span>

<span data-ttu-id="2f42a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2f42a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f42a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f42a-108">Return value</span></span>

<span data-ttu-id="2f42a-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f42a-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2f42a-110">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2f42a-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2f42a-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2f42a-111">Return code</span></span>                                                                             | <span data-ttu-id="2f42a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f42a-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="2f42a-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2f42a-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2f42a-114">La transición se ha completado.</span><span class="sxs-lookup"><span data-stu-id="2f42a-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="2f42a-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2f42a-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2f42a-116">La transición no está completa.</span><span class="sxs-lookup"><span data-stu-id="2f42a-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f42a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f42a-117">Remarks</span></span>

<span data-ttu-id="2f42a-118">Este método invalida el método [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="2f42a-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="2f42a-119">Realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f42a-119">It performs the following steps:</span></span>

-   <span data-ttu-id="2f42a-120">Llama al método **CBaseFilter::P ause** .</span><span class="sxs-lookup"><span data-stu-id="2f42a-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="2f42a-121">Confirma el asignador.</span><span class="sxs-lookup"><span data-stu-id="2f42a-121">Commits the allocator.</span></span> <span data-ttu-id="2f42a-122">(Vea [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)).</span><span class="sxs-lookup"><span data-stu-id="2f42a-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="2f42a-123">Si se detuvo el estado anterior, el filtro libera cualquier muestra que contiene.</span><span class="sxs-lookup"><span data-stu-id="2f42a-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="2f42a-124">(El ejemplo ya no es válido).</span><span class="sxs-lookup"><span data-stu-id="2f42a-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="2f42a-125">Llama al método [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) y devuelve el valor.</span><span class="sxs-lookup"><span data-stu-id="2f42a-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f42a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f42a-126">Requirements</span></span>



| <span data-ttu-id="2f42a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f42a-127">Requirement</span></span> | <span data-ttu-id="2f42a-128">Value</span><span class="sxs-lookup"><span data-stu-id="2f42a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f42a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f42a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2f42a-130"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f42a-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f42a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f42a-131">Library</span></span><br/> | <dl> <span data-ttu-id="2f42a-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f42a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f42a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f42a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f42a-134">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2f42a-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




