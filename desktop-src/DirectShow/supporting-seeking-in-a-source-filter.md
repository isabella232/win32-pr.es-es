---
description: En este tema se describe cómo implementar búsquedas en un filtro de origen de Microsoft DirectShow. Usa el ejemplo de filtro de bola como punto de partida y describe el código adicional necesario para admitir la búsqueda en este filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Admitir búsquedas en un filtro de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913138"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="d85ed-104">Admitir búsquedas en un filtro de origen</span><span class="sxs-lookup"><span data-stu-id="d85ed-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="d85ed-105">En este tema se describe cómo implementar búsquedas en un filtro de origen de Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d85ed-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="d85ed-106">Usa el ejemplo de [filtro de bola](ball-filter-sample.md) como punto de partida y describe el código adicional necesario para admitir la búsqueda en este filtro.</span><span class="sxs-lookup"><span data-stu-id="d85ed-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="d85ed-107">El ejemplo de [filtro de bola](ball-filter-sample.md) es un filtro de origen que crea una bola de rebote animado.</span><span class="sxs-lookup"><span data-stu-id="d85ed-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="d85ed-108">En este artículo se describe cómo agregar funcionalidad de búsqueda a este filtro.</span><span class="sxs-lookup"><span data-stu-id="d85ed-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="d85ed-109">Una vez que haya agregado esta funcionalidad, puede representar el filtro en GraphEdit y controlar la bola arrastrando el control deslizante de GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="d85ed-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="d85ed-110">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d85ed-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d85ed-111">Información general sobre la búsqueda en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d85ed-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="d85ed-112">Información general rápida del filtro de bola</span><span class="sxs-lookup"><span data-stu-id="d85ed-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="d85ed-113">Modificar el filtro de bola para búsquedas</span><span class="sxs-lookup"><span data-stu-id="d85ed-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="d85ed-114">Limitaciones de la clase CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="d85ed-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="d85ed-115">Información general sobre la búsqueda en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d85ed-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="d85ed-116">Una aplicación busca el gráfico de filtro llamando a un método [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="d85ed-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="d85ed-117">A continuación, el administrador de gráficos de filtro distribuye la llamada a cada representador del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d85ed-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="d85ed-118">Cada representador envía la llamada ascendente, a través del PIN de salida del siguiente filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="d85ed-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="d85ed-119">La llamada viaja hacia arriba hasta que alcanza un filtro que puede ejecutar el comando Seek, normalmente un filtro de origen o un filtro de analizador.</span><span class="sxs-lookup"><span data-stu-id="d85ed-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="d85ed-120">En general, el filtro que origina las marcas de tiempo también controla las operaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d85ed-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="d85ed-121">Un filtro responde a un comando de búsqueda de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="d85ed-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="d85ed-122">El filtro vacía el gráfico.</span><span class="sxs-lookup"><span data-stu-id="d85ed-122">The filter flushes the graph.</span></span> <span data-ttu-id="d85ed-123">Esto borra los datos obsoletos de Graph, lo que mejora la capacidad de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d85ed-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="d85ed-124">De lo contrario, es posible que se entreguen los ejemplos que se almacenaron en búfer antes del comando Seek.</span><span class="sxs-lookup"><span data-stu-id="d85ed-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="d85ed-125">El filtro llama a [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) para informar a los filtros de nivel inferior de la nueva hora de detención, la hora de inicio y la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d85ed-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="d85ed-126">Después, el filtro establece la marca de discontinuidad en el primer ejemplo después del comando Seek.</span><span class="sxs-lookup"><span data-stu-id="d85ed-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="d85ed-127">Las marcas de tiempo comienzan desde cero después de cualquier comando de búsqueda (incluidos los cambios de velocidad).</span><span class="sxs-lookup"><span data-stu-id="d85ed-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="d85ed-128">Información general rápida del filtro de bola</span><span class="sxs-lookup"><span data-stu-id="d85ed-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="d85ed-129">El filtro de bola es un origen de inserción, lo que significa que usa un subproceso de trabajo para proporcionar ejemplos de bajada, en lugar de un origen de extracción, que espera pasivamente a que un filtro de nivel inferior solicite ejemplos.</span><span class="sxs-lookup"><span data-stu-id="d85ed-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="d85ed-130">El filtro Ball se genera a partir de la clase [**CSource**](csource.md) y su PIN de salida se genera a partir de la clase [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="d85ed-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="d85ed-131">La clase **CSourceStream** crea el subproceso de trabajo que controla el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="d85ed-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="d85ed-132">Este subproceso entra en un bucle que obtiene ejemplos del asignador, los rellena con datos y los entrega de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="d85ed-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="d85ed-133">La mayor parte de la acción en [**CSourceStream**](csourcestream.md) se produce en el método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que implementa la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="d85ed-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="d85ed-134">El argumento de este método es un puntero al ejemplo que se va a entregar.</span><span class="sxs-lookup"><span data-stu-id="d85ed-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="d85ed-135">La implementación del filtro de bola de **FillBuffer** recupera la dirección del búfer de ejemplo y dibuja directamente en el búfer estableciendo valores de píxel individuales.</span><span class="sxs-lookup"><span data-stu-id="d85ed-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="d85ed-136">(El dibujo lo realiza una clase auxiliar, CBall, por lo que puede omitir los detalles relacionados con la profundidad de bits, las paletas, etc.).</span><span class="sxs-lookup"><span data-stu-id="d85ed-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="d85ed-137">Modificar el filtro de bola para búsquedas</span><span class="sxs-lookup"><span data-stu-id="d85ed-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="d85ed-138">Para que el filtro de bola sea buscable, use la clase [**CSourceSeeking**](csourceseeking.md) , que está diseñada para implementar búsquedas en filtros con un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="d85ed-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="d85ed-139">Agregue la clase **CSourceSeeking** a la lista de herencia de la clase CBallStream:</span><span class="sxs-lookup"><span data-stu-id="d85ed-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="d85ed-140">Además, tendrá que agregar un inicializador para [**CSourceSeeking**](csourceseeking.md) al constructor CBallStream:</span><span class="sxs-lookup"><span data-stu-id="d85ed-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="d85ed-141">Esta instrucción llama al constructor base de [**CSourceSeeking**](csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="d85ed-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="d85ed-142">Los parámetros son un nombre, un puntero al pin propietario, un valor **HRESULT** y la dirección de un objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="d85ed-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="d85ed-143">El nombre solo se usa para la depuración y la macro [**Name**](name.md) se compila en una cadena vacía en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="d85ed-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="d85ed-144">El PIN hereda directamente **CSourceSeeking**, por lo que el segundo parámetro es un puntero a sí mismo, convertido a un puntero [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="d85ed-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="d85ed-145">El valor **HRESULT** se omite en la versión actual de las clases base; sigue siendo compatible con las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d85ed-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="d85ed-146">La sección crítica protege los datos compartidos, como la hora de inicio actual, la hora de finalización y la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d85ed-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="d85ed-147">Agregue la siguiente instrucción en el constructor [**CSourceSeeking**](csourceseeking.md) :</span><span class="sxs-lookup"><span data-stu-id="d85ed-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="d85ed-148">La variable *m \_ rtStop* especifica la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="d85ed-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="d85ed-149">De forma predeterminada, el valor es \_ I64 \_ Max/2, que es aproximadamente 14.600 años.</span><span class="sxs-lookup"><span data-stu-id="d85ed-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="d85ed-150">La instrucción anterior lo establece en un 60 segundos más conservador.</span><span class="sxs-lookup"><span data-stu-id="d85ed-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="d85ed-151">Se deben agregar dos variables de miembro adicionales a CBallStream:</span><span class="sxs-lookup"><span data-stu-id="d85ed-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="d85ed-152">Después de cada comando de búsqueda, el filtro debe establecer la marca de discontinuidad en el ejemplo siguiente mediante una llamada a [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span><span class="sxs-lookup"><span data-stu-id="d85ed-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="d85ed-153">La variable *m \_ bDiscontinuity* realizará un seguimiento de este.</span><span class="sxs-lookup"><span data-stu-id="d85ed-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="d85ed-154">La variable *m \_ rtBallPosition* especificará la posición de la bola dentro del fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="d85ed-155">El filtro de bola original calcula la posición de la secuencia, pero el tiempo de la secuencia se restablece en cero después de cada comando de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d85ed-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="d85ed-156">En un flujo de búsqueda, la posición absoluta es independiente del tiempo de flujo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="d85ed-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="d85ed-157">QueryInterface</span></span>

<span data-ttu-id="d85ed-158">La clase [**CSourceSeeking**](csourceseeking.md) implementa la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="d85ed-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="d85ed-159">Para exponer esta interfaz a los clientes, invalide el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :</span><span class="sxs-lookup"><span data-stu-id="d85ed-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="d85ed-160">El método se denomina "sin delegación" debido a la manera en que las clases base de DirectShow admiten la agregación del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="d85ed-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="d85ed-161">Para obtener más información, vea el tema acerca de cómo implementar IUnknown en el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d85ed-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="d85ed-162">Métodos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="d85ed-162">Seeking Methods</span></span>

<span data-ttu-id="d85ed-163">La clase [**CSourceSeeking**](csourceseeking.md) mantiene varias variables de miembro relacionadas con la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d85ed-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="d85ed-164">Variable</span><span class="sxs-lookup"><span data-stu-id="d85ed-164">Variable</span></span>          | <span data-ttu-id="d85ed-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="d85ed-165">Description</span></span>   | <span data-ttu-id="d85ed-166">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d85ed-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="d85ed-167">*m \_ rtStart*</span><span class="sxs-lookup"><span data-stu-id="d85ed-167">*m\_rtStart*</span></span>      | <span data-ttu-id="d85ed-168">Hora de inicio</span><span class="sxs-lookup"><span data-stu-id="d85ed-168">Start time</span></span>    | <span data-ttu-id="d85ed-169">Cero</span><span class="sxs-lookup"><span data-stu-id="d85ed-169">Zero</span></span>           |
| <span data-ttu-id="d85ed-170">*m \_ rtStop*</span><span class="sxs-lookup"><span data-stu-id="d85ed-170">*m\_rtStop*</span></span>       | <span data-ttu-id="d85ed-171">Hora de detención</span><span class="sxs-lookup"><span data-stu-id="d85ed-171">Stop time</span></span>     | <span data-ttu-id="d85ed-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="d85ed-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="d85ed-173">*m \_ dRateSeeking*</span><span class="sxs-lookup"><span data-stu-id="d85ed-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="d85ed-174">Velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="d85ed-174">Playback rate</span></span> | <span data-ttu-id="d85ed-175">1,0</span><span class="sxs-lookup"><span data-stu-id="d85ed-175">1.0</span></span>            |



 

<span data-ttu-id="d85ed-176">La implementación de [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) actualiza las horas de inicio y de finalización y, a continuación, llama a dos métodos virtuales puros en la clase derivada, [**CSourceSeeking:: cambie las**](csourceseeking-changestart.md) y [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="d85ed-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="d85ed-177">La implementación de [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) es similar: actualiza la velocidad de reproducción y, a continuación, llama al método virtual puro [**CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="d85ed-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="d85ed-178">En cada uno de estos métodos virtuales, el PIN debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d85ed-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="d85ed-179">Llame a [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) para iniciar el vaciado de datos.</span><span class="sxs-lookup"><span data-stu-id="d85ed-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="d85ed-180">Detenga el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="d85ed-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="d85ed-181">Llame a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="d85ed-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="d85ed-182">Reinicie el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="d85ed-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="d85ed-183">Llame a [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="d85ed-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="d85ed-184">Establezca la marca de discontinuidad en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d85ed-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="d85ed-185">El orden de estos pasos es fundamental, ya que el subproceso de streaming puede bloquearse mientras espera para ofrecer un ejemplo u obtener un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="d85ed-186">El método [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantiza que el subproceso de streaming no está bloqueado y, por lo tanto, no interbloqueará en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="d85ed-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="d85ed-187">La llamada a [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa a los filtros de nivel inferior para que esperen nuevos ejemplos, por lo que no los rechazan cuando el subproceso vuelve a iniciarse en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="d85ed-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="d85ed-188">El siguiente método privado realiza los pasos 1 a 4:</span><span class="sxs-lookup"><span data-stu-id="d85ed-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="d85ed-189">Cuando el subproceso de streaming se vuelve a iniciar, llama al método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) .</span><span class="sxs-lookup"><span data-stu-id="d85ed-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="d85ed-190">Invalide este método para realizar los pasos 5 y 6:</span><span class="sxs-lookup"><span data-stu-id="d85ed-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="d85ed-191">En el método [**cambie las**](csourceseeking-changestart.md) , establezca la hora de la secuencia en cero y la posición de la bola en la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="d85ed-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="d85ed-192">Después, llame a CBallStream:: UpdateFromSeek:</span><span class="sxs-lookup"><span data-stu-id="d85ed-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="d85ed-193">En el método [**ChangeStop**](csourceseeking-changestop.md) , llame a CBallStream:: UpdateFromSeek si la nueva hora de detención es menor que la posición actual.</span><span class="sxs-lookup"><span data-stu-id="d85ed-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="d85ed-194">De lo contrario, la hora de detención todavía está en el futuro, por lo que no es necesario vaciar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="d85ed-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="d85ed-195">En el caso de los cambios de velocidad, el método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) establece *m \_ dRateSeeking* en la nueva velocidad (descartando el valor anterior) antes de llamar a [**ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="d85ed-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="d85ed-196">Desafortunadamente, si el autor de la llamada dio una tasa no válida (por ejemplo, menor que cero), es demasiado tarde en el momento en que se llama a **ChangeRate** .</span><span class="sxs-lookup"><span data-stu-id="d85ed-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="d85ed-197">Una solución consiste en invalidar **SetRate** y comprobar las tarifas válidas:</span><span class="sxs-lookup"><span data-stu-id="d85ed-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="d85ed-198">Dibujar en el búfer</span><span class="sxs-lookup"><span data-stu-id="d85ed-198">Drawing in the Buffer</span></span>

<span data-ttu-id="d85ed-199">Esta es la versión modificada de [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md), la rutina que dibuja la bola en cada fotograma:</span><span class="sxs-lookup"><span data-stu-id="d85ed-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="d85ed-200">Las principales diferencias entre esta versión y la original son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d85ed-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="d85ed-201">Como se mencionó anteriormente, la variable *m \_ rtBallPosition* se usa para establecer la posición de la bola, en lugar de la hora de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d85ed-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="d85ed-202">Después de mantener la sección crítica, el método comprueba si la posición actual supera la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="d85ed-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="d85ed-203">Si es así, devuelve **S \_ false**, que indica a la clase base que detenga el envío de datos y entregue una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d85ed-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="d85ed-204">Las marcas de tiempo se dividen por la velocidad actual.</span><span class="sxs-lookup"><span data-stu-id="d85ed-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="d85ed-205">Si *m \_ BDiscontinuity* es **true**, el método establece la marca de discontinuidad en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="d85ed-206">Hay otra diferencia secundaria.</span><span class="sxs-lookup"><span data-stu-id="d85ed-206">There is another minor difference.</span></span> <span data-ttu-id="d85ed-207">Dado que la versión original se basa en tener exactamente un búfer, rellena todo el búfer con ceros una vez, cuando comienza el streaming.</span><span class="sxs-lookup"><span data-stu-id="d85ed-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="d85ed-208">Después, simplemente borra la bola de su posición anterior.</span><span class="sxs-lookup"><span data-stu-id="d85ed-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="d85ed-209">Sin embargo, esta optimización revela un ligero error en el filtro de bola.</span><span class="sxs-lookup"><span data-stu-id="d85ed-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="d85ed-210">Cuando el método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) llama a [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), establece la marca de solo lectura en **false**.</span><span class="sxs-lookup"><span data-stu-id="d85ed-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="d85ed-211">Como resultado, el filtro de nivel inferior es libre de escribir en el búfer.</span><span class="sxs-lookup"><span data-stu-id="d85ed-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="d85ed-212">Una solución consiste en invalidar **DecideAllocator** para que establezca la marca de solo lectura en **true**.</span><span class="sxs-lookup"><span data-stu-id="d85ed-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="d85ed-213">Para simplificar, sin embargo, la nueva versión simplemente quita la optimización por completo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="d85ed-214">En su lugar, esta versión rellena el búfer con ceros cada vez.</span><span class="sxs-lookup"><span data-stu-id="d85ed-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="d85ed-215">Cambios varios</span><span class="sxs-lookup"><span data-stu-id="d85ed-215">Miscellaneous Changes</span></span>

<span data-ttu-id="d85ed-216">En la nueva versión, estas dos líneas se quitan del constructor CBall:</span><span class="sxs-lookup"><span data-stu-id="d85ed-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="d85ed-217">El filtro de bola original utiliza estos valores para agregar cierta aleatoriedad a la posición inicial de la bola.</span><span class="sxs-lookup"><span data-stu-id="d85ed-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="d85ed-218">Para nuestros propósitos, queremos que la bola sea determinista.</span><span class="sxs-lookup"><span data-stu-id="d85ed-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="d85ed-219">Además, se han cambiado algunas variables de los objetos [**CRefTime**](creftime.md) a variables de [**\_ tiempo de referencia**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="d85ed-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="d85ed-220">(La clase **CRefTime** es un contenedor fino para un valor de **\_ hora de referencia** ). Por último, la implementación de [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) se ha modificado ligeramente; puede hacer referencia al código fuente para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d85ed-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="d85ed-221">Limitaciones de la clase CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="d85ed-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="d85ed-222">La clase [**CSourceSeeking**](csourceseeking.md) no está diseñada para los filtros con varios PIN de salida, debido a problemas con la comunicación entre PIN.</span><span class="sxs-lookup"><span data-stu-id="d85ed-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="d85ed-223">Por ejemplo, Imagine un filtro de analizador que reciba una secuencia de audio y vídeo intercalada, divida el flujo en sus componentes de audio y vídeo, y entregue el vídeo de un PIN de salida y el audio de otro.</span><span class="sxs-lookup"><span data-stu-id="d85ed-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="d85ed-224">Ambos pines de salida recibirán todos los comandos de búsqueda, pero el filtro solo debe buscar una vez por cada comando de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d85ed-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="d85ed-225">La solución consiste en designar uno de los pin para controlar la búsqueda y omitir los comandos de búsqueda recibidos por el otro PIN.</span><span class="sxs-lookup"><span data-stu-id="d85ed-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="d85ed-226">Sin embargo, después del comando Seek, ambos PIN deben vaciar los datos.</span><span class="sxs-lookup"><span data-stu-id="d85ed-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="d85ed-227">Para complicar aún más los aspectos, el comando Seek se produce en el subproceso de la aplicación, no en el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="d85ed-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="d85ed-228">Por lo tanto, debe asegurarse de que ninguno de los pin esté bloqueado y en espera de que se devuelva una llamada [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , o podría producirse un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="d85ed-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="d85ed-229">Para obtener más información sobre el vaciado seguro para subprocesos en PIN, vea [subprocesos y secciones críticas](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="d85ed-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d85ed-230">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d85ed-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d85ed-231">Escribir filtros de origen</span><span class="sxs-lookup"><span data-stu-id="d85ed-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



