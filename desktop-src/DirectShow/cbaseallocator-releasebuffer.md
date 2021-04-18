---
description: 'El método ReleaseBuffer devuelve un ejemplo multimedia a la lista de ejemplos de medios disponibles. Este método implementa el método IMemAllocator:: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690811"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="1acb1-104">CBaseAllocator. ReleaseBuffer, método</span><span class="sxs-lookup"><span data-stu-id="1acb1-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="1acb1-105">El `ReleaseBuffer` método devuelve un ejemplo multimedia a la lista de ejemplos de medios disponibles.</span><span class="sxs-lookup"><span data-stu-id="1acb1-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="1acb1-106">Este método implementa el método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="1acb1-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acb1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1acb1-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="1acb1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1acb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1acb1-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="1acb1-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="1acb1-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del objeto de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="1acb1-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1acb1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1acb1-111">Return value</span></span>

<span data-ttu-id="1acb1-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="1acb1-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1acb1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1acb1-113">Remarks</span></span>

<span data-ttu-id="1acb1-114">Cuando el recuento de referencias de un ejemplo multimedia llega a cero, el ejemplo llama a **ReleaseBuffer** con sí mismo como parámetro.</span><span class="sxs-lookup"><span data-stu-id="1acb1-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="1acb1-115">Este método realiza las acciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="1acb1-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="1acb1-116">Devuelve el ejemplo de medio a la lista libre ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="1acb1-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="1acb1-117">Llama al método [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , que libera todos los subprocesos que están bloqueados en llamadas al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1acb1-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="1acb1-118">Si se llamó previamente al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) , llama al método **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .</span><span class="sxs-lookup"><span data-stu-id="1acb1-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="1acb1-119">Cuando se libera la última muestra, si hay una llamada pendiente [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , llama al método [**CBaseAllocator:: Free**](cbaseallocator-free.md) para liberar la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="1acb1-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="1acb1-120">(En la clase base, **Free** es un método virtual puro).</span><span class="sxs-lookup"><span data-stu-id="1acb1-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="1acb1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1acb1-121">Requirements</span></span>



| <span data-ttu-id="1acb1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acb1-122">Requirement</span></span> | <span data-ttu-id="1acb1-123">Value</span><span class="sxs-lookup"><span data-stu-id="1acb1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acb1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1acb1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1acb1-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1acb1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1acb1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1acb1-126">Library</span></span><br/> | <dl> <span data-ttu-id="1acb1-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1acb1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1acb1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1acb1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acb1-129">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="1acb1-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




