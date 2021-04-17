---
description: La clase CPosPassThru controla los comandos de búsqueda para los filtros de transformación, pasándolos al siguiente filtro.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Clase CPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670905"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="e5cbe-103">Clase CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="e5cbe-103">CPosPassThru class</span></span>

![jerarquía de clase base cpospassthru](images/cutil14.png)

<span data-ttu-id="e5cbe-105">La `CPosPassThru` clase controla los comandos de búsqueda para los filtros de transformación, pasándolos al siguiente filtro.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="e5cbe-106">Cuando una aplicación busca el gráfico de filtro, el administrador de gráficos de filtro proporciona el comando de búsqueda a los filtros de representador.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="e5cbe-107">El comando se pasa hacia arriba, a través de la clavija de salida de cada filtro hasta que alcanza un filtro que puede ejecutar el comando (si existe).</span><span class="sxs-lookup"><span data-stu-id="e5cbe-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="e5cbe-108">Para obtener más información, vea [Buscar](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="e5cbe-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="e5cbe-109">La `CPosPassThru` clase pasa todos los comandos de búsqueda al terminal de salida en el filtro de nivel superior, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![la clase cpospassthru envía comandos de búsqueda ascendentes.](images/cpospassthru.png)

<span data-ttu-id="e5cbe-111">Aunque esta clase se proporciona en la biblioteca de clases base, DirectShow también proporciona la misma clase en Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="e5cbe-112">El uso de la versión de Quartz.dll puede reducir ligeramente el tamaño del código en el filtro, porque la clase se carga en tiempo de ejecución desde el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="e5cbe-113">Para usar esa versión, llame a la función [**CreatePosPassThru**](createpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="e5cbe-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="e5cbe-114">En el método **NonDelegatingQueryInterface** del PIN de salida, delegue en el objeto **CPosPassThru** siempre que la interfaz solicitada sea [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e5cbe-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="e5cbe-115">Excepto donde se indique lo contrario, todos los métodos [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de esta clase llaman al método correspondiente en el PIN conectado y devuelven el resultado.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="e5cbe-116">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e5cbe-116">Public Methods</span></span>                                                    | <span data-ttu-id="e5cbe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5cbe-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5cbe-118">**CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="e5cbe-119">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="e5cbe-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="e5cbe-121">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="e5cbe-122">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="e5cbe-123">Recupera las marcas de tiempo en el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="e5cbe-124">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-124">Virtual.</span></span>                                           |
| <span data-ttu-id="e5cbe-125">Métodos IMediaPosition</span><span class="sxs-lookup"><span data-stu-id="e5cbe-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="e5cbe-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5cbe-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5cbe-127">**obtener \_ duración**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="e5cbe-128">Recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="e5cbe-129">**Put \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="e5cbe-130">Establece la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="e5cbe-131">**obtener \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="e5cbe-132">Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="e5cbe-133">**Put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="e5cbe-134">Establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="e5cbe-135">**obtener \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="e5cbe-136">Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="e5cbe-137">**Put \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="e5cbe-138">Establece la cantidad de datos que se pondrán en cola antes de la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="e5cbe-139">**obtener \_ velocidad**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="e5cbe-140">Recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="e5cbe-141">**\_tasa Put**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="e5cbe-142">Establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="e5cbe-143">**obtener \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="e5cbe-144">Recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="e5cbe-145">**CanSeekForward**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="e5cbe-146">Determina si la secuencia se puede buscar hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="e5cbe-147">**CanSeekBackward**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="e5cbe-148">Determina si se puede buscar en el flujo hacia delante.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="e5cbe-149">Métodos IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="e5cbe-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="e5cbe-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5cbe-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5cbe-151">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="e5cbe-152">Consulta si un flujo tiene capacidades de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="e5cbe-153">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="e5cbe-154">Convierte de un formato de hora a otro.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="e5cbe-155">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="e5cbe-156">Recupera el intervalo de veces que la búsqueda es eficaz.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="e5cbe-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="e5cbe-158">Recupera todas las funciones de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="e5cbe-159">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="e5cbe-160">Recupera la posición actual, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="e5cbe-161">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="e5cbe-162">Recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="e5cbe-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="e5cbe-164">Recupera la posición actual y la posición de detención, en relación con la duración total de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="e5cbe-165">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="e5cbe-166">Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="e5cbe-167">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="e5cbe-168">Recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="e5cbe-169">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="e5cbe-170">Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="e5cbe-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="e5cbe-172">Recupera el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="e5cbe-173">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="e5cbe-174">Determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="e5cbe-175">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="e5cbe-176">Determina si un formato de hora especificado es el formato que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="e5cbe-177">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="e5cbe-178">Recupera el formato de hora preferido para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="e5cbe-179">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="e5cbe-180">Establece la posición actual y la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="e5cbe-181">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="e5cbe-182">Establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="e5cbe-183">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="e5cbe-184">Establece el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="e5cbe-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="e5cbe-185">Funciones del asistente</span><span class="sxs-lookup"><span data-stu-id="e5cbe-185">Helper Functions</span></span>                                                  | <span data-ttu-id="e5cbe-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5cbe-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5cbe-187">**CreatePosPassThru**</span><span class="sxs-lookup"><span data-stu-id="e5cbe-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="e5cbe-188">Crea un `CPosPassThru` objeto o [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="e5cbe-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="e5cbe-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5cbe-189">Requirements</span></span>



| <span data-ttu-id="e5cbe-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5cbe-190">Requirement</span></span> | <span data-ttu-id="e5cbe-191">Value</span><span class="sxs-lookup"><span data-stu-id="e5cbe-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cbe-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5cbe-192">Header</span></span><br/>  | <dl> <span data-ttu-id="e5cbe-193"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5cbe-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5cbe-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5cbe-194">Library</span></span><br/> | <dl> <span data-ttu-id="e5cbe-195"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e5cbe-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




