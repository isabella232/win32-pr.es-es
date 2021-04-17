---
description: La clase CBaseOutputPin es una clase base abstracta que implementa un PIN de salida.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Clase CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660982"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="d5655-103">Clase CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="d5655-103">CBaseOutputPin class</span></span>

![jerarquía de clases cbaseoutputpin](images/filter06.png)

<span data-ttu-id="d5655-105">La `CBaseOutputPin` clase es una clase base abstracta que implementa un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="d5655-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="d5655-106">Esta clase se deriva de [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="d5655-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="d5655-107">Difiere de **CBasePin** en los siguientes aspectos:</span><span class="sxs-lookup"><span data-stu-id="d5655-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="d5655-108">Solo se conecta a los pin de entrada que admiten la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="d5655-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="d5655-109">Admite el transporte de memoria local a través de la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="d5655-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="d5655-110">Rechaza las notificaciones de final de secuencia, vaciado y segmento nuevo.</span><span class="sxs-lookup"><span data-stu-id="d5655-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="d5655-111">(Estos no se deben enviar a un PIN de salida).</span><span class="sxs-lookup"><span data-stu-id="d5655-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="d5655-112">Proporciona métodos para entregar ejemplos de bajada.</span><span class="sxs-lookup"><span data-stu-id="d5655-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="d5655-113">Cuando el PIN se conecta, solicita un asignador de memoria del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5655-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="d5655-114">Si no es así, se crea un nuevo objeto de asignador.</span><span class="sxs-lookup"><span data-stu-id="d5655-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="d5655-115">El PIN de salida es responsable de establecer las propiedades de asignador.</span><span class="sxs-lookup"><span data-stu-id="d5655-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="d5655-116">Para ello, se realiza el método virtual puro [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="d5655-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="d5655-117">Invalide este método en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="d5655-117">Override this method in your derived class.</span></span> <span data-ttu-id="d5655-118">Si el PIN de entrada tiene algún requisito de búfer, se pasan al método **DecideBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="d5655-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="d5655-119">Llame al método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un ejemplo de medio vacío.</span><span class="sxs-lookup"><span data-stu-id="d5655-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="d5655-120">Llame al método [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) para proporcionar ejemplos de bajada.</span><span class="sxs-lookup"><span data-stu-id="d5655-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="d5655-121">La clase derivada debe reemplazar el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro para validar el tipo de medio durante las conexiones del PIN.</span><span class="sxs-lookup"><span data-stu-id="d5655-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="d5655-122">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="d5655-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="d5655-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5655-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="d5655-124">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="d5655-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="d5655-125">Puntero al asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="d5655-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="d5655-126">**m \_ pInputPin**</span><span class="sxs-lookup"><span data-stu-id="d5655-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="d5655-127">Puntero al pin de entrada conectado a este pin.</span><span class="sxs-lookup"><span data-stu-id="d5655-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="d5655-128">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="d5655-128">Public Methods</span></span>                                                  | <span data-ttu-id="d5655-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5655-129">Description</span></span>                                                                |
| [<span data-ttu-id="d5655-130">**CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d5655-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="d5655-131">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="d5655-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="d5655-132">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="d5655-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="d5655-133">Completa una conexión a un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5655-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="d5655-134">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-134">Virtual.</span></span>                           |
| [<span data-ttu-id="d5655-135">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="d5655-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="d5655-136">Selecciona un asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="d5655-136">Selects a memory allocator.</span></span> <span data-ttu-id="d5655-137">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="d5655-138">**GetDeliveryBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5655-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="d5655-139">Recupera un ejemplo multimedia que contiene un búfer vacío.</span><span class="sxs-lookup"><span data-stu-id="d5655-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="d5655-140">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-140">Virtual.</span></span>           |
| [<span data-ttu-id="d5655-141">**Entrega**</span><span class="sxs-lookup"><span data-stu-id="d5655-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="d5655-142">Entrega un ejemplo multimedia a la clavija de entrada conectada.</span><span class="sxs-lookup"><span data-stu-id="d5655-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="d5655-143">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-143">Virtual.</span></span>               |
| [<span data-ttu-id="d5655-144">**InitAllocator**</span><span class="sxs-lookup"><span data-stu-id="d5655-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="d5655-145">Crea un asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="d5655-145">Creates a memory allocator.</span></span> <span data-ttu-id="d5655-146">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="d5655-147">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="d5655-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="d5655-148">Determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="d5655-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="d5655-149">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="d5655-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="d5655-150">Libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="d5655-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="d5655-151">**Active**</span><span class="sxs-lookup"><span data-stu-id="d5655-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="d5655-152">Notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="d5655-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="d5655-153">**Inactivo**</span><span class="sxs-lookup"><span data-stu-id="d5655-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="d5655-154">Notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="d5655-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="d5655-155">**DeliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d5655-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="d5655-156">Entrega una notificación de final de secuencia a la clavija de entrada conectada. Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="d5655-157">**DeliverBeginFlush**</span><span class="sxs-lookup"><span data-stu-id="d5655-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="d5655-158">Solicita la clavija de entrada conectada para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d5655-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="d5655-159">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-159">Virtual.</span></span>      |
| [<span data-ttu-id="d5655-160">**DeliverEndFlush**</span><span class="sxs-lookup"><span data-stu-id="d5655-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="d5655-161">Solicita la clavija de entrada conectada para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d5655-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="d5655-162">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-162">Virtual.</span></span>        |
| [<span data-ttu-id="d5655-163">**DeliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="d5655-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="d5655-164">Entrega una notificación de nuevo segmento al pin de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="d5655-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="d5655-165">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="d5655-165">Virtual.</span></span>   |
| <span data-ttu-id="d5655-166">Métodos virtuales puros</span><span class="sxs-lookup"><span data-stu-id="d5655-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="d5655-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5655-167">Description</span></span>                                                                |
| [<span data-ttu-id="d5655-168">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="d5655-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="d5655-169">Establece los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="d5655-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="d5655-170">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="d5655-170">IPin Methods</span></span>                                                    | <span data-ttu-id="d5655-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5655-171">Description</span></span>                                                                |
| [<span data-ttu-id="d5655-172">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="d5655-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="d5655-173">Comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d5655-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="d5655-174">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="d5655-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="d5655-175">Finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d5655-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="d5655-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d5655-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="d5655-177">Notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="d5655-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="d5655-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5655-178">Requirements</span></span>



| <span data-ttu-id="d5655-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5655-179">Requirement</span></span> | <span data-ttu-id="d5655-180">Value</span><span class="sxs-lookup"><span data-stu-id="d5655-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5655-181">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5655-181">Header</span></span><br/>  | <dl> <span data-ttu-id="d5655-182"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5655-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5655-183">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5655-183">Library</span></span><br/> | <dl> <span data-ttu-id="d5655-184"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d5655-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




