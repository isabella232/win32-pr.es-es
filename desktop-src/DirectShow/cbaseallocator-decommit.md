---
description: El método de anulación de confirmación anula el asignador. Este método implementa el método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator. decommit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660619"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="c119d-104">CBaseAllocator. decommit (método)</span><span class="sxs-lookup"><span data-stu-id="c119d-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="c119d-105">El `Decommit` método anula la confirmación del asignador.</span><span class="sxs-lookup"><span data-stu-id="c119d-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="c119d-106">Este método implementa el método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .</span><span class="sxs-lookup"><span data-stu-id="c119d-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c119d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c119d-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="c119d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c119d-108">Parameters</span></span>

<span data-ttu-id="c119d-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c119d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c119d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c119d-110">Return value</span></span>

<span data-ttu-id="c119d-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c119d-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c119d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c119d-112">Remarks</span></span>

<span data-ttu-id="c119d-113">Después de llamar a este método, se producirá un error en las llamadas al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c119d-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="c119d-114">A medida que se publican los ejemplos, se devuelven a la lista de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c119d-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="c119d-115">Cuando se devuelve la última muestra, el asignador llama al método [**CBaseAllocator:: Free**](cbaseallocator-free.md) , que libera la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="c119d-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="c119d-116">(En la clase base, **Free** es un método virtual puro).</span><span class="sxs-lookup"><span data-stu-id="c119d-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="c119d-117">Además, este método libera todos los subprocesos que están bloqueados en llamadas a **getBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c119d-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="c119d-118">Se produce un error en las llamadas a **getBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c119d-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c119d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c119d-119">Requirements</span></span>



| <span data-ttu-id="c119d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c119d-120">Requirement</span></span> | <span data-ttu-id="c119d-121">Value</span><span class="sxs-lookup"><span data-stu-id="c119d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c119d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c119d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c119d-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c119d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c119d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c119d-124">Library</span></span><br/> | <dl> <span data-ttu-id="c119d-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c119d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c119d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c119d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c119d-127">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="c119d-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




