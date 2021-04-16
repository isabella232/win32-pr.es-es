---
description: El método Run ejecuta el filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Método CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671729"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="21a58-103">CBaseRenderer. Run (método)</span><span class="sxs-lookup"><span data-stu-id="21a58-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="21a58-104">El `Run` método ejecuta el filtro.</span><span class="sxs-lookup"><span data-stu-id="21a58-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21a58-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="21a58-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21a58-106">Parameters</span></span>

<span data-ttu-id="21a58-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="21a58-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21a58-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21a58-108">Return value</span></span>

<span data-ttu-id="21a58-109">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="21a58-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a58-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21a58-110">Remarks</span></span>

<span data-ttu-id="21a58-111">Este método invalida el método [**CBaseFilter:: Run**](cbasefilter-run.md) .</span><span class="sxs-lookup"><span data-stu-id="21a58-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="21a58-112">Las acciones que realiza son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="21a58-112">It performs the following actions:</span></span>

-   <span data-ttu-id="21a58-113">Llama al método **CBaseFilter:: Run** .</span><span class="sxs-lookup"><span data-stu-id="21a58-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="21a58-114">Confirma el asignador.</span><span class="sxs-lookup"><span data-stu-id="21a58-114">Commits the allocator.</span></span> <span data-ttu-id="21a58-115">(Vea [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)).</span><span class="sxs-lookup"><span data-stu-id="21a58-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="21a58-116">Si se detuvo el estado anterior, el filtro libera cualquier muestra que contiene.</span><span class="sxs-lookup"><span data-stu-id="21a58-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="21a58-117">(El ejemplo ya no es válido).</span><span class="sxs-lookup"><span data-stu-id="21a58-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="21a58-118">Llama al método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="21a58-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="21a58-119">Si hay un ejemplo pendiente, el método **StartStreaming** lo programa para su representación.</span><span class="sxs-lookup"><span data-stu-id="21a58-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="21a58-120">Si el filtro no está conectado, publica un evento [**de \_ finalización de EC**](ec-complete.md) inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="21a58-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a58-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21a58-121">Requirements</span></span>



| <span data-ttu-id="21a58-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a58-122">Requirement</span></span> | <span data-ttu-id="21a58-123">Value</span><span class="sxs-lookup"><span data-stu-id="21a58-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a58-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21a58-124">Header</span></span><br/>  | <dl> <span data-ttu-id="21a58-125"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21a58-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21a58-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21a58-126">Library</span></span><br/> | <dl> <span data-ttu-id="21a58-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="21a58-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a58-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="21a58-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a58-129">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="21a58-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




