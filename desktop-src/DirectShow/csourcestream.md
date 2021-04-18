---
description: La clase CSourceStream proporciona un PIN de salida para la clase de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Clase CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680598"
---
# <a name="csourcestream-class"></a><span data-ttu-id="b8be8-103">Clase CSourceStream</span><span class="sxs-lookup"><span data-stu-id="b8be8-103">CSourceStream class</span></span>

![jerarquía de clases csourcestream](images/source02.png)

<span data-ttu-id="b8be8-105">La clase **CSourceStream** proporciona un PIN de salida para la clase de filtro [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="b8be8-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="b8be8-106">Para obtener información sobre el uso de esta clase, vea [**CSource**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="b8be8-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="b8be8-107">Esta clase hereda la clase [**CAMThread**](camthread.md) , que proporciona un subproceso de trabajo para el streaming de datos del PIN.</span><span class="sxs-lookup"><span data-stu-id="b8be8-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="b8be8-108">La clase **CSourceStream** implementa los siguientes métodos auxiliares para enviar solicitudes al subproceso:</span><span class="sxs-lookup"><span data-stu-id="b8be8-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="b8be8-109">**CSourceStream:: Exit**</span><span class="sxs-lookup"><span data-stu-id="b8be8-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="b8be8-110">**CSourceStream:: init**</span><span class="sxs-lookup"><span data-stu-id="b8be8-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="b8be8-111">**CSourceStream::P ause**</span><span class="sxs-lookup"><span data-stu-id="b8be8-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="b8be8-112">**CSourceStream:: Run**</span><span class="sxs-lookup"><span data-stu-id="b8be8-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="b8be8-113">**CSourceStream:: Stop**</span><span class="sxs-lookup"><span data-stu-id="b8be8-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="b8be8-114">La primera solicitud al subproceso debe ser [**init**](csourcestream-init.md).</span><span class="sxs-lookup"><span data-stu-id="b8be8-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="b8be8-115">La solicitud de [**salida**](csourcestream-exit.md) finaliza el subproceso.</span><span class="sxs-lookup"><span data-stu-id="b8be8-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="b8be8-116">En la práctica, no es necesario llamar a cualquiera de estos métodos directamente, ya que los métodos [**CSourceStream:: Active**](csourcestream-active.md) y [**CSourceStream:: Inactive**](csourcestream-inactive.md) del PIN los llaman según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b8be8-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="b8be8-117">La clase también proporciona varios métodos de "controlador":</span><span class="sxs-lookup"><span data-stu-id="b8be8-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="b8be8-118">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="b8be8-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="b8be8-119">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="b8be8-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="b8be8-120">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="b8be8-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="b8be8-121">No hacen nada en la clase base, pero la clase derivada puede invalidarlos.</span><span class="sxs-lookup"><span data-stu-id="b8be8-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="b8be8-122">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="b8be8-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="b8be8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8be8-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8be8-124">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="b8be8-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="b8be8-125">Puntero al filtro que contiene este pin.</span><span class="sxs-lookup"><span data-stu-id="b8be8-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="b8be8-126">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="b8be8-126">Protected Methods</span></span>                                                      | <span data-ttu-id="b8be8-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8be8-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="b8be8-128">**OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="b8be8-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="b8be8-129">Se llama cuando se inicializa el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="b8be8-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="b8be8-130">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="b8be8-131">**OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="b8be8-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="b8be8-132">Se llama cuando el subproceso de streaming está a punto de salir.</span><span class="sxs-lookup"><span data-stu-id="b8be8-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="b8be8-133">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="b8be8-134">**OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="b8be8-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="b8be8-135">Se llama al principio del método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="b8be8-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="b8be8-136">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-136">Virtual.</span></span> |
| [<span data-ttu-id="b8be8-137">**Active**</span><span class="sxs-lookup"><span data-stu-id="b8be8-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="b8be8-138">Notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="b8be8-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="b8be8-139">**Inactivo**</span><span class="sxs-lookup"><span data-stu-id="b8be8-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="b8be8-140">Notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="b8be8-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="b8be8-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="b8be8-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="b8be8-142">Espera a la siguiente solicitud de subproceso.</span><span class="sxs-lookup"><span data-stu-id="b8be8-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="b8be8-143">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="b8be8-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="b8be8-144">Comprueba si hay una solicitud de subproceso, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="b8be8-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="b8be8-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="b8be8-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="b8be8-146">Procedimiento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="b8be8-146">Thread procedure.</span></span> <span data-ttu-id="b8be8-147">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="b8be8-148">**DoBufferProcessingLoop**</span><span class="sxs-lookup"><span data-stu-id="b8be8-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="b8be8-149">Genera datos multimedia y los entrega al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b8be8-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="b8be8-150">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="b8be8-151">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="b8be8-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="b8be8-152">Determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="b8be8-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="b8be8-153">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="b8be8-154">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="b8be8-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="b8be8-155">Recupera un tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="b8be8-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="b8be8-156">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="b8be8-157">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="b8be8-157">Public Methods</span></span>                                                         | <span data-ttu-id="b8be8-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8be8-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="b8be8-159">**CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="b8be8-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="b8be8-160">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="b8be8-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="b8be8-161">**~ CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="b8be8-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="b8be8-162">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="b8be8-162">Destructor method.</span></span> <span data-ttu-id="b8be8-163">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="b8be8-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="b8be8-164">**Smss**</span><span class="sxs-lookup"><span data-stu-id="b8be8-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="b8be8-165">Inicializa el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="b8be8-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="b8be8-166">**Salir**</span><span class="sxs-lookup"><span data-stu-id="b8be8-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="b8be8-167">Indica al subproceso de streaming que salga.</span><span class="sxs-lookup"><span data-stu-id="b8be8-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="b8be8-168">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="b8be8-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="b8be8-169">Indica al subproceso de streaming que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="b8be8-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="b8be8-170">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="b8be8-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="b8be8-171">Indica al subproceso de streaming que se active.</span><span class="sxs-lookup"><span data-stu-id="b8be8-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="b8be8-172">**Stop**</span><span class="sxs-lookup"><span data-stu-id="b8be8-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="b8be8-173">Indica al subproceso de streaming que se detenga.</span><span class="sxs-lookup"><span data-stu-id="b8be8-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="b8be8-174">Métodos virtuales puros</span><span class="sxs-lookup"><span data-stu-id="b8be8-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="b8be8-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8be8-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="b8be8-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="b8be8-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="b8be8-177">Rellena un ejemplo multimedia con datos.</span><span class="sxs-lookup"><span data-stu-id="b8be8-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="b8be8-178">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="b8be8-178">IPin Methods</span></span>                                                           | <span data-ttu-id="b8be8-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8be8-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="b8be8-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="b8be8-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="b8be8-181">Recupera un identificador para el código PIN.</span><span class="sxs-lookup"><span data-stu-id="b8be8-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="b8be8-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8be8-182">Requirements</span></span>



| <span data-ttu-id="b8be8-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8be8-183">Requirement</span></span> | <span data-ttu-id="b8be8-184">Value</span><span class="sxs-lookup"><span data-stu-id="b8be8-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8be8-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8be8-185">Header</span></span><br/>  | <dl> <span data-ttu-id="b8be8-186"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8be8-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b8be8-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8be8-187">Library</span></span><br/> | <dl> <span data-ttu-id="b8be8-188"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b8be8-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8be8-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8be8-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8be8-190">Escribir filtros de origen</span><span class="sxs-lookup"><span data-stu-id="b8be8-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




