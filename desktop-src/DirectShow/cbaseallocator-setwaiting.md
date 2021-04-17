---
description: El método SetWaiting incrementa el número de subprocesos en espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator. SetWaiting (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661125"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="b96bf-103">CBaseAllocator. SetWaiting, método</span><span class="sxs-lookup"><span data-stu-id="b96bf-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="b96bf-104">El `SetWaiting` método incrementa el recuento de subprocesos en espera.</span><span class="sxs-lookup"><span data-stu-id="b96bf-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b96bf-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="b96bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b96bf-106">Parameters</span></span>

<span data-ttu-id="b96bf-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b96bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b96bf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b96bf-108">Return value</span></span>

<span data-ttu-id="b96bf-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b96bf-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b96bf-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b96bf-110">Remarks</span></span>

<span data-ttu-id="b96bf-111">Este método incrementa la variable miembro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="b96bf-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="b96bf-112">Si un subproceso está bloqueado en el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) , el asignador llama a `SetWaiting` y, a continuación, espera a que se Señalice el semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="b96bf-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="b96bf-113">El método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) señala el semáforo y establece *m \_ lWaiting* en cero.</span><span class="sxs-lookup"><span data-stu-id="b96bf-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b96bf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b96bf-114">Requirements</span></span>



| <span data-ttu-id="b96bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b96bf-115">Requirement</span></span> | <span data-ttu-id="b96bf-116">Value</span><span class="sxs-lookup"><span data-stu-id="b96bf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b96bf-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b96bf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b96bf-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b96bf-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b96bf-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b96bf-119">Library</span></span><br/> | <dl> <span data-ttu-id="b96bf-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b96bf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b96bf-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b96bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96bf-122">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="b96bf-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




