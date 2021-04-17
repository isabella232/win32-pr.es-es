---
description: 'El método GetBuffer recupera un ejemplo multimedia que contiene un búfer. Este método implementa el método IMemAllocator:: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Método CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661131"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="45afe-104">CBaseAllocator. GetBuffer, método</span><span class="sxs-lookup"><span data-stu-id="45afe-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="45afe-105">El `GetBuffer` método recupera un ejemplo multimedia que contiene un búfer.</span><span class="sxs-lookup"><span data-stu-id="45afe-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="45afe-106">Este método implementa el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="45afe-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45afe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45afe-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="45afe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45afe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45afe-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="45afe-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="45afe-110">Recibe un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del búfer.</span><span class="sxs-lookup"><span data-stu-id="45afe-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="45afe-111">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="45afe-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="45afe-112">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="45afe-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="45afe-113">Puntero a la hora de inicio del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45afe-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="45afe-114">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="45afe-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="45afe-115">Puntero a la hora de finalización del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="45afe-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="45afe-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="45afe-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="45afe-117">Combinación bit a bit de cero o más marcadores.</span><span class="sxs-lookup"><span data-stu-id="45afe-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="45afe-118">La clase base admite la siguiente marca.</span><span class="sxs-lookup"><span data-stu-id="45afe-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="45afe-119">Value</span><span class="sxs-lookup"><span data-stu-id="45afe-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="45afe-120">Significado</span><span class="sxs-lookup"><span data-stu-id="45afe-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="45afe-121"><dt>**AM \_ GBF \_ nowait**</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="45afe-122">No espere a que un búfer esté disponible.</span><span class="sxs-lookup"><span data-stu-id="45afe-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45afe-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45afe-123">Return value</span></span>

<span data-ttu-id="45afe-124">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45afe-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="45afe-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45afe-125">Return code</span></span>                                                                                           | <span data-ttu-id="45afe-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="45afe-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="45afe-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="45afe-128">Correcto.</span><span class="sxs-lookup"><span data-stu-id="45afe-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="45afe-129"><dt>**VFW \_ E \_ no \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="45afe-130">No se confirmó el asignador.</span><span class="sxs-lookup"><span data-stu-id="45afe-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="45afe-131"><dt>**tiempo de espera de VFW \_ E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="45afe-132">agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="45afe-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="45afe-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45afe-133">Remarks</span></span>

<span data-ttu-id="45afe-134">A menos que el llamador especifique la marca **AM \_ GBF \_ nowait** en *dwFlags*, este método se bloquea hasta que esté disponible la siguiente muestra.</span><span class="sxs-lookup"><span data-stu-id="45afe-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="45afe-135">El ejemplo de medio recuperado tiene un puntero válido al búfer asignado.</span><span class="sxs-lookup"><span data-stu-id="45afe-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="45afe-136">El autor de la llamada es responsable de establecer las demás propiedades del ejemplo, como las marcas de tiempo, las horas del medio o la propiedad de punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="45afe-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="45afe-137">Para obtener más información, vea [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="45afe-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="45afe-138">En la clase base, se omiten los parámetros *pStartTime* y *pEndTime* .</span><span class="sxs-lookup"><span data-stu-id="45afe-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="45afe-139">Las clases derivadas pueden utilizar estos valores.</span><span class="sxs-lookup"><span data-stu-id="45afe-139">Derived classes can use these values.</span></span> <span data-ttu-id="45afe-140">Por ejemplo, el asignador del filtro de [representador de vídeo](video-renderer-filter.md) usa estos valores para sincronizar el cambio entre las superficies de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="45afe-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="45afe-141">Si el método necesita esperar en un ejemplo, incrementa el recuento de objetos en espera ([**CBaseAllocator:: m \_ lCount**](cbaseallocator-m-lcount.md)) y llama a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) en el semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="45afe-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="45afe-142">Cuando una muestra está disponible, llama al método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) en el asignador, lo que aumenta el recuento de semáforos por **m \_ lCount** (con lo que se liberan los subprocesos en espera) y vuelve a establecer **m \_ lCount** en cero.</span><span class="sxs-lookup"><span data-stu-id="45afe-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="45afe-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45afe-143">Requirements</span></span>



| <span data-ttu-id="45afe-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="45afe-144">Requirement</span></span> | <span data-ttu-id="45afe-145">Value</span><span class="sxs-lookup"><span data-stu-id="45afe-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45afe-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45afe-146">Header</span></span><br/>  | <dl> <span data-ttu-id="45afe-147"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45afe-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45afe-148">Library</span></span><br/> | <dl> <span data-ttu-id="45afe-149"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="45afe-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45afe-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="45afe-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45afe-151">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="45afe-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

