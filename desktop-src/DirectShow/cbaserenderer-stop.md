---
description: El método Stop detiene el filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Método CBaseRenderer. STOP (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661268"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="ac631-103">CBaseRenderer. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="ac631-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="ac631-104">El `Stop` método detiene el filtro.</span><span class="sxs-lookup"><span data-stu-id="ac631-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac631-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac631-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="ac631-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac631-106">Parameters</span></span>

<span data-ttu-id="ac631-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ac631-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac631-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac631-108">Return value</span></span>

<span data-ttu-id="ac631-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ac631-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac631-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac631-110">Remarks</span></span>

<span data-ttu-id="ac631-111">Este método invalida el método [**CBaseFilter:: Stop**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="ac631-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="ac631-112">Las acciones que realiza son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ac631-112">It performs the following actions:</span></span>

-   <span data-ttu-id="ac631-113">Llama a [**CBaseFilter:: Stop**](cbasefilter-stop.md).</span><span class="sxs-lookup"><span data-stu-id="ac631-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="ac631-114">Anula la confirmación del asignador.</span><span class="sxs-lookup"><span data-stu-id="ac631-114">Decommits the allocator.</span></span> <span data-ttu-id="ac631-115">(Consulte [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)).</span><span class="sxs-lookup"><span data-stu-id="ac631-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="ac631-116">Cancela cualquier representación programada y libera el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="ac631-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="ac631-117">Espera a que se complete cualquier llamada de **recepción** pendiente.</span><span class="sxs-lookup"><span data-stu-id="ac631-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac631-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac631-118">Requirements</span></span>



| <span data-ttu-id="ac631-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac631-119">Requirement</span></span> | <span data-ttu-id="ac631-120">Value</span><span class="sxs-lookup"><span data-stu-id="ac631-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac631-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac631-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ac631-122"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac631-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ac631-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac631-123">Library</span></span><br/> | <dl> <span data-ttu-id="ac631-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ac631-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac631-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac631-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac631-126">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ac631-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




