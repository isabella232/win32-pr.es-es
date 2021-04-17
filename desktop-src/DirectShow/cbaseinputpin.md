---
description: La clase CBaseInputPin es una clase base abstracta para implementar clavijas de entrada. Esta clase agrega compatibilidad para la interfaz IMemInputPin, además de la compatibilidad con la interfaz IPin proporcionada por CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Clase CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670953"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="dcf20-104">Clase CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="dcf20-104">CBaseInputPin class</span></span>

![jerarquía de clases cbaseinputpin](images/filter07.png)

<span data-ttu-id="dcf20-106">La `CBaseInputPin` clase es una clase base abstracta para implementar clavijas de entrada.</span><span class="sxs-lookup"><span data-stu-id="dcf20-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="dcf20-107">Esta clase agrega compatibilidad para la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , además de la compatibilidad con la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) proporcionada por [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="dcf20-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="dcf20-108">Para usar esta clase, derive una nueva clase e invalide al menos los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="dcf20-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="dcf20-109">**CBaseInputPin::BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="dcf20-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="dcf20-110">**CBaseInputPin::EndFlush**</span><span class="sxs-lookup"><span data-stu-id="dcf20-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="dcf20-111">**CBaseInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="dcf20-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="dcf20-112">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcf20-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="dcf20-113">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcf20-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="dcf20-114">Dependiendo de la función del PIN, es posible que deba invalidar métodos adicionales en `CBaseInputPin` o **CBasePin**.</span><span class="sxs-lookup"><span data-stu-id="dcf20-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="dcf20-115">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="dcf20-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="dcf20-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf20-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcf20-117">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="dcf20-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="dcf20-118">Puntero al asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="dcf20-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="dcf20-119">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="dcf20-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="dcf20-120">Marca que indica si el asignador genera ejemplos de medios de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dcf20-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="dcf20-121">**m \_ bFlushing**</span><span class="sxs-lookup"><span data-stu-id="dcf20-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="dcf20-122">Marca que indica si el PIN se está vaciando actualmente.</span><span class="sxs-lookup"><span data-stu-id="dcf20-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="dcf20-123">**m \_ SampleProps**</span><span class="sxs-lookup"><span data-stu-id="dcf20-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="dcf20-124">Propiedades de la muestra más reciente.</span><span class="sxs-lookup"><span data-stu-id="dcf20-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="dcf20-125">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="dcf20-125">Public Methods</span></span>                                                             | <span data-ttu-id="dcf20-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf20-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="dcf20-127">**CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="dcf20-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="dcf20-128">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="dcf20-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="dcf20-129">**~ CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="dcf20-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="dcf20-130">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="dcf20-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="dcf20-131">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="dcf20-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="dcf20-132">Libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="dcf20-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="dcf20-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="dcf20-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="dcf20-134">Consulta si el asignador usa ejemplos de medios de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dcf20-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="dcf20-135">**IsFlushing**</span><span class="sxs-lookup"><span data-stu-id="dcf20-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="dcf20-136">Consulta si el filtro se está vaciando actualmente.</span><span class="sxs-lookup"><span data-stu-id="dcf20-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="dcf20-137">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="dcf20-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="dcf20-138">Determina si el pin puede aceptar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="dcf20-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="dcf20-139">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="dcf20-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="dcf20-140">**PassNotify**</span><span class="sxs-lookup"><span data-stu-id="dcf20-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="dcf20-141">Pasa un mensaje de control de calidad al objeto adecuado.</span><span class="sxs-lookup"><span data-stu-id="dcf20-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="dcf20-142">**Inactivo**</span><span class="sxs-lookup"><span data-stu-id="dcf20-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="dcf20-143">Notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="dcf20-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="dcf20-144">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="dcf20-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="dcf20-145">**SampleProps**</span><span class="sxs-lookup"><span data-stu-id="dcf20-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="dcf20-146">Recupera las propiedades del ejemplo más reciente.</span><span class="sxs-lookup"><span data-stu-id="dcf20-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="dcf20-147">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="dcf20-147">IPin Methods</span></span>                                                               | <span data-ttu-id="dcf20-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf20-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="dcf20-149">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="dcf20-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="dcf20-150">Comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="dcf20-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="dcf20-151">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="dcf20-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="dcf20-152">Finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="dcf20-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="dcf20-153">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="dcf20-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="dcf20-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf20-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="dcf20-155">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="dcf20-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="dcf20-156">Recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="dcf20-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="dcf20-157">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="dcf20-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="dcf20-158">Especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="dcf20-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="dcf20-159">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="dcf20-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="dcf20-160">Recupera las propiedades de asignador solicitadas por el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="dcf20-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="dcf20-161">**Aparecen**</span><span class="sxs-lookup"><span data-stu-id="dcf20-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="dcf20-162">Recibe el siguiente ejemplo multimedia en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="dcf20-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="dcf20-163">**ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="dcf20-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="dcf20-164">Recibe varios ejemplos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="dcf20-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="dcf20-165">**ReceiveCanBlock**</span><span class="sxs-lookup"><span data-stu-id="dcf20-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="dcf20-166">Determina si las llamadas al método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) podrían bloquearse.</span><span class="sxs-lookup"><span data-stu-id="dcf20-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="dcf20-167">Métodos IQualityControl</span><span class="sxs-lookup"><span data-stu-id="dcf20-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="dcf20-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf20-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="dcf20-169">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="dcf20-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="dcf20-170">Recibe un mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="dcf20-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="dcf20-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf20-171">Requirements</span></span>



| <span data-ttu-id="dcf20-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf20-172">Requirement</span></span> | <span data-ttu-id="dcf20-173">Value</span><span class="sxs-lookup"><span data-stu-id="dcf20-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf20-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcf20-174">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf20-175"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcf20-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dcf20-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcf20-176">Library</span></span><br/> | <dl> <span data-ttu-id="dcf20-177"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dcf20-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




