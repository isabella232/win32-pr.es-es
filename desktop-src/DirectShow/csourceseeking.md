---
description: La clase CSourceSeeking es una clase abstracta para implementar búsquedas en filtros de origen con un PIN de salida.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Clase CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690511"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="c7648-103">Clase CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="c7648-103">CSourceSeeking class</span></span>

![jerarquía de clases csourceseeking](images/cutil15.png)

<span data-ttu-id="c7648-105">La clase **CSourceSeeking** es una clase abstracta para implementar búsquedas en filtros de origen con un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="c7648-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="c7648-106">Esta clase es compatible con la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="c7648-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="c7648-107">Proporciona implementaciones predeterminadas para todos los métodos **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="c7648-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="c7648-108">Las variables miembro protegidas almacenan la hora de inicio, la hora de detención y la tasa actual.</span><span class="sxs-lookup"><span data-stu-id="c7648-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="c7648-109">De forma predeterminada, el único formato de hora admitido por la clase es el **formato de hora \_ \_ media \_ Time** (unidades 100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="c7648-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="c7648-110">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c7648-110">See Remarks for more information.</span></span>



| <span data-ttu-id="c7648-111">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="c7648-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="c7648-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7648-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7648-113">**m \_ rtDuration**</span><span class="sxs-lookup"><span data-stu-id="c7648-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="c7648-114">Duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c7648-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="c7648-115">**m \_ rtStart**</span><span class="sxs-lookup"><span data-stu-id="c7648-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="c7648-116">Hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="c7648-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="c7648-117">**m \_ rtStop**</span><span class="sxs-lookup"><span data-stu-id="c7648-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="c7648-118">Hora de detención.</span><span class="sxs-lookup"><span data-stu-id="c7648-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="c7648-119">**m \_ dRateSeeking**</span><span class="sxs-lookup"><span data-stu-id="c7648-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="c7648-120">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c7648-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="c7648-121">**m \_ dwSeekingCaps**</span><span class="sxs-lookup"><span data-stu-id="c7648-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="c7648-122">Funciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7648-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="c7648-123">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="c7648-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="c7648-124">Puntero a un objeto de sección crítica para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="c7648-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="c7648-125">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="c7648-125">Protected Methods</span></span>                                                   | <span data-ttu-id="c7648-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7648-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="c7648-127">**CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="c7648-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="c7648-128">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="c7648-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="c7648-129">Métodos virtuales puros</span><span class="sxs-lookup"><span data-stu-id="c7648-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="c7648-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7648-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="c7648-131">**ChangeRate**</span><span class="sxs-lookup"><span data-stu-id="c7648-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="c7648-132">Se le llama cuando cambia la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c7648-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="c7648-133">**Cambie las**</span><span class="sxs-lookup"><span data-stu-id="c7648-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="c7648-134">Se le llama cuando cambia la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="c7648-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="c7648-135">**ChangeStop**</span><span class="sxs-lookup"><span data-stu-id="c7648-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="c7648-136">Se le llama cuando cambia la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="c7648-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="c7648-137">Métodos IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="c7648-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="c7648-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7648-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="c7648-139">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="c7648-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="c7648-140">Determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="c7648-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="c7648-141">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="c7648-142">Recupera el formato de hora preferido del objeto.</span><span class="sxs-lookup"><span data-stu-id="c7648-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="c7648-143">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="c7648-144">Establece el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="c7648-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="c7648-145">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="c7648-146">Determina si un formato de hora especificado es el formato que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="c7648-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="c7648-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="c7648-148">Recupera el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="c7648-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="c7648-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="c7648-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="c7648-150">Recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c7648-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="c7648-151">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="c7648-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="c7648-152">Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c7648-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="c7648-153">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="c7648-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="c7648-154">Recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c7648-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="c7648-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c7648-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="c7648-156">Recupera todas las funciones de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c7648-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="c7648-157">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c7648-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="c7648-158">Consulta si la secuencia tiene capacidades de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="c7648-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="c7648-159">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="c7648-160">Convierte de un formato de hora a otro.</span><span class="sxs-lookup"><span data-stu-id="c7648-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="c7648-161">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="c7648-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="c7648-162">Establece la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="c7648-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="c7648-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="c7648-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="c7648-164">Recupera la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="c7648-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="c7648-165">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="c7648-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="c7648-166">Recupera el intervalo de veces que la búsqueda es eficaz.</span><span class="sxs-lookup"><span data-stu-id="c7648-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="c7648-167">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="c7648-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="c7648-168">Establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c7648-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="c7648-169">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="c7648-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="c7648-170">Recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c7648-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="c7648-171">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="c7648-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="c7648-172">Recupera el tiempo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="c7648-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c7648-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7648-173">Remarks</span></span>

<span data-ttu-id="c7648-174">Cuando cambia la posición de inicio, la posición de detención o la velocidad de reproducción, el objeto **CSourceSeeking** llama al método virtual puro correspondiente:</span><span class="sxs-lookup"><span data-stu-id="c7648-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="c7648-175">Posición inicial: [ **CSourceSeeking:: cambie las**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="c7648-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="c7648-176">Posición de detención: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="c7648-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="c7648-177">Velocidad de reproducción: [ **CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="c7648-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="c7648-178">La clase derivada debe implementar estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c7648-178">The derived class must implement these methods.</span></span> <span data-ttu-id="c7648-179">Después de cualquier operación de búsqueda, un filtro debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c7648-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="c7648-180">Llame al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="c7648-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="c7648-181">Detenga el subproceso de trabajo que está entregando datos.</span><span class="sxs-lookup"><span data-stu-id="c7648-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="c7648-182">Llame al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7648-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="c7648-183">Reinicie el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c7648-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="c7648-184">Llame al método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7648-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="c7648-185">Establezca la propiedad discontinuidad en el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c7648-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="c7648-186">Llame al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="c7648-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="c7648-187">La llamada a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libera el subproceso de trabajo, si el subproceso está bloqueado en espera para ofrecer un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c7648-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="c7648-188">En el paso 2, asegúrese de que el subproceso ha dejado de enviar datos.</span><span class="sxs-lookup"><span data-stu-id="c7648-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="c7648-189">Dependiendo de la implementación, puede que tenga que esperar a que el subproceso se cierre o para que el subproceso señale una respuesta de algún tipo.</span><span class="sxs-lookup"><span data-stu-id="c7648-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="c7648-190">Si el filtro usa la clase [**CSourceStream**](csourcestream.md) , el método [**CSourceStream:: Stop**](csourcestream-stop.md) se bloquea hasta que el subproceso de trabajo responde.</span><span class="sxs-lookup"><span data-stu-id="c7648-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="c7648-191">Idealmente, el nuevo segmento (paso 5) debe entregarse desde el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c7648-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="c7648-192">También lo puede hacer el objeto **CSourceSeeking** , siempre y cuando el filtro lo serialice con los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c7648-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="c7648-193">En el ejemplo siguiente se muestra una posible implementación.</span><span class="sxs-lookup"><span data-stu-id="c7648-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="c7648-194">Se supone que el PIN de salida del filtro de origen se deriva de **CSourceSeeking** y [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="c7648-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="c7648-195">En este ejemplo se define un método auxiliar, UpdateFromSeek, que realiza los pasos 1 4.</span><span class="sxs-lookup"><span data-stu-id="c7648-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="c7648-196">El método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) se invalida para enviar el nuevo segmento y para establecer una marca que indica la discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="c7648-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="c7648-197">El subproceso de trabajo recoge esta marca y llama al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :</span><span class="sxs-lookup"><span data-stu-id="c7648-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="c7648-198">Compatibilidad con formatos de hora adicionales</span><span class="sxs-lookup"><span data-stu-id="c7648-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="c7648-199">De forma predeterminada, esta clase admite la búsqueda solo en unidades de tiempo de referencia ( \_ tiempo medio de formato de tiempo \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="c7648-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="c7648-200">Para admitir formatos de hora adicionales, invalide los métodos de [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que se ocupan de los formatos de hora:</span><span class="sxs-lookup"><span data-stu-id="c7648-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="c7648-201">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="c7648-202">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="c7648-203">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="c7648-204">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="c7648-205">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c7648-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="c7648-206">Además, invalide los métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes para realizar las conversiones necesarias entre los formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="c7648-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="c7648-207">Después de llamar al método [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , todos los métodos **IMediaSeeking** deben tratar los parámetros de tiempo de entrada y de salida como si estuvieran en el nuevo formato de hora.</span><span class="sxs-lookup"><span data-stu-id="c7648-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="c7648-208">Por ejemplo, si la variable *m \_ rtDuration* representa la duración en unidades de tiempo de referencia, pero el formato de hora actual es fotogramas, el método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) debe devolver el valor *m \_ rtDuration* convertido a fotogramas.</span><span class="sxs-lookup"><span data-stu-id="c7648-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="c7648-209">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c7648-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="c7648-210">Además, asegúrese de comprobar la \_ marca AM Seek \_ ReturnTime en el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="c7648-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="c7648-211">Si este marcador está presente, convierta los valores de posición en tiempos de referencia cuando los devuelva al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c7648-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7648-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7648-212">Requirements</span></span>



| <span data-ttu-id="c7648-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7648-213">Requirement</span></span> | <span data-ttu-id="c7648-214">Value</span><span class="sxs-lookup"><span data-stu-id="c7648-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7648-215">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7648-215">Header</span></span><br/>  | <dl> <span data-ttu-id="c7648-216"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7648-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7648-217">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7648-217">Library</span></span><br/> | <dl> <span data-ttu-id="c7648-218"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c7648-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7648-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7648-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7648-220">Admitir búsquedas en un filtro de origen</span><span class="sxs-lookup"><span data-stu-id="c7648-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




