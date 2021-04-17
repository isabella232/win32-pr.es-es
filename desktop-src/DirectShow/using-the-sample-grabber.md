---
description: El filtro de enganche de ejemplo es un filtro de transformación que se puede usar para obtener ejemplos de medios de un flujo a medida que pasan por el gráfico de filtro.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Usar el enganche de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678080"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="be35e-103">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="be35e-103">Using the Sample Grabber</span></span>

<span data-ttu-id="be35e-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="be35e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="be35e-105">El filtro de [**enganche de ejemplo**](sample-grabber-filter.md) es un filtro de transformación que se puede usar para obtener ejemplos de medios de un flujo a medida que pasan por el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="be35e-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="be35e-106">Si simplemente desea captar un mapa de bits de un archivo de vídeo, es más fácil usar el objeto de [detector de medios (MediaDet)](media-detector--mediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="be35e-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="be35e-107">Consulte [captación de un fotograma de póster](grabbing-a-poster-frame.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="be35e-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="be35e-108">Sin embargo, el captador de ejemplo es más flexible porque funciona con casi cualquier tipo de medio (vea [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) para las pocas excepciones) y ofrece más control a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="be35e-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="be35e-109">Crear el administrador de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="be35e-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="be35e-110">Agregar el captador de ejemplo al gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="be35e-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="be35e-111">Establecer el tipo de medio</span><span class="sxs-lookup"><span data-stu-id="be35e-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="be35e-112">Crear el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="be35e-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="be35e-113">Ejecutar el gráfico</span><span class="sxs-lookup"><span data-stu-id="be35e-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="be35e-114">Captar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="be35e-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="be35e-115">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="be35e-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="be35e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be35e-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="be35e-117">Crear el administrador de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="be35e-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="be35e-118">Para empezar, cree el [Administrador de gráficos de filtro](filter-graph-manager.md) y consulte las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="be35e-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="be35e-119">Agregar el captador de ejemplo al gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="be35e-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="be35e-120">Cree una instancia del filtro de enganche de ejemplo y addit al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="be35e-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="be35e-121">Consulte el filtro de enganche de ejemplo para la interfaz [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="be35e-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="be35e-122">Establecer el tipo de medio</span><span class="sxs-lookup"><span data-stu-id="be35e-122">Set the Media Type</span></span>

<span data-ttu-id="be35e-123">La primera vez que se crea el enganche de ejemplo, no tiene ningún tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="be35e-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="be35e-124">Esto significa que puede conectarse a casi cualquier filtro del gráfico, pero no tendrá ningún control sobre el tipo de datos que recibió.</span><span class="sxs-lookup"><span data-stu-id="be35e-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="be35e-125">Antes de compilar el resto del gráfico, por lo tanto, debe establecer un tipo de medio para el enganche de ejemplo llamando al método [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="be35e-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="be35e-126">Cuando se conecte el enganche de ejemplo, comparará este tipo de medio con el tipo de medio ofrecido por el otro filtro.</span><span class="sxs-lookup"><span data-stu-id="be35e-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="be35e-127">Los únicos campos que comprueba son el tipo principal, el subtipo y el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="be35e-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="be35e-128">Para cualquiera de ellos, el valor \_ null GUID significa "Accept any Value".</span><span class="sxs-lookup"><span data-stu-id="be35e-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="be35e-129">La mayoría de las veces, querrá establecer el tipo y el subtipo principales.</span><span class="sxs-lookup"><span data-stu-id="be35e-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="be35e-130">Por ejemplo, el código siguiente especifica el vídeo RGB de 24 bits sin comprimir:</span><span class="sxs-lookup"><span data-stu-id="be35e-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="be35e-131">Crear el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="be35e-131">Build the Filter Graph</span></span>

<span data-ttu-id="be35e-132">Ahora puede compilar el resto del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="be35e-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="be35e-133">Dado que el enganche de ejemplo solo se conectará con el tipo de medio que ha especificado, le permite aprovechar los mecanismos de [conexión inteligente](intelligent-connect.md) del administrador de gráficos de filtro al compilar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="be35e-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="be35e-134">Por ejemplo, si especificó vídeo sin comprimir, puede conectar un filtro de origen al enganche de ejemplo y el administrador de gráficos de filtros agregará automáticamente el analizador de archivos y el descodificador.</span><span class="sxs-lookup"><span data-stu-id="be35e-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="be35e-135">En el ejemplo siguiente se usa la función auxiliar ConnectFilters, que se muestra en [conectar dos filtros](connect-two-filters.md):</span><span class="sxs-lookup"><span data-stu-id="be35e-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="be35e-136">El enganche de ejemplo es un filtro de transformación, por lo que el PIN de salida debe estar conectado a otro filtro.</span><span class="sxs-lookup"><span data-stu-id="be35e-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="be35e-137">A menudo, puede que simplemente desee descartar los ejemplos después de que haya terminado con ellos.</span><span class="sxs-lookup"><span data-stu-id="be35e-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="be35e-138">En ese caso, conecte el captador de muestra al [**filtro de representador nulo**](null-renderer-filter.md), que descarta los datos que recibe.</span><span class="sxs-lookup"><span data-stu-id="be35e-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="be35e-139">En el ejemplo siguiente se conecta el captador de ejemplo al filtro de representador nulo:</span><span class="sxs-lookup"><span data-stu-id="be35e-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="be35e-140">Tenga en cuenta que colocar el captador de ejemplo entre un descodificador de vídeo y el representador de vídeo puede perjudicar significativamente el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="be35e-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="be35e-141">El enganche de ejemplo es un filtro de transferencia en contexto, lo que significa que el búfer de salida es el mismo que el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="be35e-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="be35e-142">Para la representación de vídeo, es probable que el búfer de salida se encuentre en la tarjeta gráfica, donde las operaciones de lectura son mucho más lentas, en comparación con las operaciones de lectura en la memoria principal.</span><span class="sxs-lookup"><span data-stu-id="be35e-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="be35e-143">Ejecutar el gráfico</span><span class="sxs-lookup"><span data-stu-id="be35e-143">Run the Graph</span></span>

<span data-ttu-id="be35e-144">El enganche de ejemplo funciona en uno de los dos modos siguientes:</span><span class="sxs-lookup"><span data-stu-id="be35e-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="be35e-145">El modo de almacenamiento en búfer realiza una copia de cada ejemplo antes de entregar el ejemplo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="be35e-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="be35e-146">El modo de devolución de llamada invoca una función de devolución de llamada definida por la aplicación en cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="be35e-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="be35e-147">En este artículo se describe el modo de almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="be35e-147">This article describes buffering mode.</span></span> <span data-ttu-id="be35e-148">(Antes de usar el modo de devolución de llamada, tenga en cuenta que la función de devolución de llamada debe estar bastante limitada.</span><span class="sxs-lookup"><span data-stu-id="be35e-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="be35e-149">De lo contrario, puede reducir drásticamente el rendimiento o incluso causar interbloqueos.</span><span class="sxs-lookup"><span data-stu-id="be35e-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="be35e-150">Para obtener más información, vea [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md)). Para activar el modo de almacenamiento en búfer, llame al método [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="be35e-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="be35e-151">Opcionalmente, llame al método [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="be35e-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="be35e-152">Esto hace que el captador de ejemplo se detenga después de recibir el primer ejemplo multimedia, lo que resulta útil si desea captar un solo fotograma de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="be35e-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="be35e-153">Busque el tiempo deseado, ejecute el gráfico y espere hasta el evento de [**\_ finalización de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="be35e-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="be35e-154">Tenga en cuenta que el nivel de precisión del marco depende del origen.</span><span class="sxs-lookup"><span data-stu-id="be35e-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="be35e-155">Por ejemplo, la búsqueda de un archivo MPEG suele ser una precisión de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="be35e-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="be35e-156">Para ejecutar el gráfico lo más rápido posible, convierta el reloj del gráfico como se describe en [establecer el reloj del gráfico](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="be35e-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="be35e-157">En el ejemplo siguiente se habilita el modo de una sola captura y el modo de almacenamiento en búfer, se ejecuta el gráfico de filtro y se espera a que finalice.</span><span class="sxs-lookup"><span data-stu-id="be35e-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="be35e-158">Captar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="be35e-158">Grab the Sample</span></span>

<span data-ttu-id="be35e-159">En el modo de almacenamiento en búfer, el enganche de ejemplo almacena una copia de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="be35e-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="be35e-160">El método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia el búfer en una matriz asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="be35e-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="be35e-161">Para determinar el tamaño de la matriz que se necesita, llame primero a **GetCurrentBuffer** con un puntero **nulo** para la dirección de la matriz.</span><span class="sxs-lookup"><span data-stu-id="be35e-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="be35e-162">A continuación, asigne la matriz y llame a la segunda vez al método para copiar el búfer.</span><span class="sxs-lookup"><span data-stu-id="be35e-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="be35e-163">En el ejemplo siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="be35e-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="be35e-164">Tendrá que conocer el formato exacto de los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="be35e-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="be35e-165">Para obtener esta información, llame al método [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="be35e-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="be35e-166">Este método rellena una estructura de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con el formato.</span><span class="sxs-lookup"><span data-stu-id="be35e-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="be35e-167">En el caso de una secuencia de vídeo sin comprimir, la información de formato se encuentra en una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="be35e-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="be35e-168">En el ejemplo siguiente se muestra cómo obtener la información de formato de una secuencia de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="be35e-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="be35e-169">El enganche de ejemplo no es compatible con [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="be35e-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="be35e-170">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="be35e-170">Example Code</span></span>

<span data-ttu-id="be35e-171">Este es el código completo de los ejemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="be35e-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="be35e-172">En este ejemplo se usa la función [SafeRelease](../medfound/saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="be35e-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="be35e-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be35e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be35e-174">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="be35e-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
