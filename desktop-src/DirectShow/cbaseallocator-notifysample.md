---
description: El método NotifySample libera todos los subprocesos que están esperando ejemplos.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Método CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671475"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="32518-103">CBaseAllocator. NotifySample, método</span><span class="sxs-lookup"><span data-stu-id="32518-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="32518-104">El `NotifySample` método libera todos los subprocesos que están esperando ejemplos.</span><span class="sxs-lookup"><span data-stu-id="32518-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="32518-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32518-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="32518-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32518-106">Parameters</span></span>

<span data-ttu-id="32518-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="32518-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32518-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32518-108">Return value</span></span>

<span data-ttu-id="32518-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="32518-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32518-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32518-110">Remarks</span></span>

<span data-ttu-id="32518-111">Cuando hay subprocesos en espera de ejemplos, el valor de [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) es mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="32518-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="32518-112">Si *m \_ lWaiting* es mayor que cero, este método llama a la función **ReleaseSemaphore (** en el semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , activando los subprocesos en espera.</span><span class="sxs-lookup"><span data-stu-id="32518-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="32518-113">También restablece *m \_ lWaiting* en cero.</span><span class="sxs-lookup"><span data-stu-id="32518-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="32518-114">Se llama a este método desde el método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , cuando se devuelve un ejemplo a la lista libre. y del método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , cuando se desconfirma el asignador.</span><span class="sxs-lookup"><span data-stu-id="32518-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="32518-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32518-115">Requirements</span></span>



| <span data-ttu-id="32518-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="32518-116">Requirement</span></span> | <span data-ttu-id="32518-117">Value</span><span class="sxs-lookup"><span data-stu-id="32518-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32518-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32518-118">Header</span></span><br/>  | <dl> <span data-ttu-id="32518-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32518-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32518-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32518-120">Library</span></span><br/> | <dl> <span data-ttu-id="32518-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="32518-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32518-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="32518-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32518-123">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="32518-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




