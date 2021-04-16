---
description: Controlar un gráfico de captura
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlar un gráfico de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537677"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="b78d7-103">Controlar un gráfico de captura</span><span class="sxs-lookup"><span data-stu-id="b78d7-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="b78d7-104">La interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) del administrador de gráficos de filtro tiene métodos para ejecutar, detener y pausar todo el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b78d7-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="b78d7-105">Sin embargo, si el gráfico de filtros tiene secuencias de captura y vista previa, es probable que desee controlar los dos flujos de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="b78d7-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="b78d7-106">Por ejemplo, puede que desee obtener una vista previa del vídeo sin capturarlo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="b78d7-107">Puede hacerlo a través del método [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .</span><span class="sxs-lookup"><span data-stu-id="b78d7-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="b78d7-108">Este método no funciona al capturar en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="b78d7-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="b78d7-109">Controlar el flujo de captura</span><span class="sxs-lookup"><span data-stu-id="b78d7-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="b78d7-110">El código siguiente establece la secuencia de captura de vídeo para que se ejecute durante cuatro segundos, empezando un segundo después de que se ejecute el gráfico:</span><span class="sxs-lookup"><span data-stu-id="b78d7-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="b78d7-111">El primer parámetro especifica la secuencia que se va a controlar, como un GUID de categoría de PIN.</span><span class="sxs-lookup"><span data-stu-id="b78d7-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="b78d7-112">El segundo parámetro proporciona el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b78d7-112">The second parameter gives the media type.</span></span> <span data-ttu-id="b78d7-113">El tercer parámetro es un puntero al filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="b78d7-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="b78d7-114">Para controlar todas las secuencias de captura en el gráfico, establezca el segundo y el tercer parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="b78d7-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="b78d7-115">Los dos parámetros siguientes definen las horas en que se iniciará y detendrá la secuencia, en relación con la hora a la que se inicia la ejecución del gráfico.</span><span class="sxs-lookup"><span data-stu-id="b78d7-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="b78d7-116">Llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b78d7-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="b78d7-117">Hasta que se ejecute el gráfico, el método **ControlStream** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b78d7-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="b78d7-118">Si el gráfico ya se está ejecutando, la configuración surte efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b78d7-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="b78d7-119">Los dos últimos parámetros se usan para obtener notificaciones de eventos cuando el flujo se inicia y se detiene.</span><span class="sxs-lookup"><span data-stu-id="b78d7-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="b78d7-120">Para cada secuencia que controla mediante este método, el gráfico de filtros envía un par de eventos: el [**control de secuencia de EC se \_ \_ \_ inicia**](ec-stream-control-started.md) cuando se inicia el flujo y el [**control de secuencia de EC se \_ \_ \_ detiene**](ec-stream-control-stopped.md) cuando se detiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b78d7-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="b78d7-121">Los valores de **wStartCookie** y **wStopCookie** se usan como el segundo parámetro de evento.</span><span class="sxs-lookup"><span data-stu-id="b78d7-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="b78d7-122">Por lo tanto, *lParam2* en el evento Start es igual a **wStartCookie** y *lParam2* en el evento STOP es igual a **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="b78d7-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="b78d7-123">En el código siguiente se muestra cómo obtener estos eventos:</span><span class="sxs-lookup"><span data-stu-id="b78d7-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="b78d7-124">El método **ControlStream** define algunos valores especiales para las horas de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="b78d7-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="b78d7-125">Start</span><span class="sxs-lookup"><span data-stu-id="b78d7-125">Start</span></span>                                  | <span data-ttu-id="b78d7-126">Stop</span><span class="sxs-lookup"><span data-stu-id="b78d7-126">Stop</span></span>                               |
| <span data-ttu-id="b78d7-127">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="b78d7-127">MAXLONGLONG</span></span> | <span data-ttu-id="b78d7-128">Nunca inicie esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="b78d7-128">Never start this stream.</span></span>               | <span data-ttu-id="b78d7-129">No se detenga hasta que el gráfico se detenga.</span><span class="sxs-lookup"><span data-stu-id="b78d7-129">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="b78d7-130">**NULL**</span><span class="sxs-lookup"><span data-stu-id="b78d7-130">**NULL**</span></span>    | <span data-ttu-id="b78d7-131">Iniciar inmediatamente cuando se ejecuta el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b78d7-131">Start immediately when the graph runs.</span></span> | <span data-ttu-id="b78d7-132">Detener inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b78d7-132">Stop immediately.</span></span>                  |



 

<span data-ttu-id="b78d7-133">Por ejemplo, el código siguiente detiene inmediatamente el flujo de captura:</span><span class="sxs-lookup"><span data-stu-id="b78d7-133">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b78d7-134">Aunque puede detener el flujo de captura y reiniciarlo más adelante, se creará una brecha en las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-134">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="b78d7-135">En la reproducción, el vídeo parecerá que se detiene durante el intervalo (en función del formato de archivo).</span><span class="sxs-lookup"><span data-stu-id="b78d7-135">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="b78d7-136">Controlar la secuencia de vista previa</span><span class="sxs-lookup"><span data-stu-id="b78d7-136">Controlling the Preview Stream</span></span>

<span data-ttu-id="b78d7-137">Para controlar el PIN de vista previa, llame a **ControlStream** , pero establezca el primer parámetro en la \_ versión preliminar de la categoría PIN \_ .</span><span class="sxs-lookup"><span data-stu-id="b78d7-137">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="b78d7-138">Esto funciona igual que en \_ la captura de categoría de PIN \_ , salvo que no se pueden utilizar tiempos de referencia para especificar el inicio y la detención, ya que los marcos de vista previa no tienen marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-138">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="b78d7-139">Por lo tanto, debe usar **null** o MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="b78d7-139">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="b78d7-140">Use **null** para iniciar la secuencia de vista previa:</span><span class="sxs-lookup"><span data-stu-id="b78d7-140">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b78d7-141">Use MAXLONGLONG para detener la secuencia de vista previa:</span><span class="sxs-lookup"><span data-stu-id="b78d7-141">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b78d7-142">No importa si la secuencia de vista previa proviene de un PIN de vista previa en el filtro de captura o del filtro de forma inteligente.</span><span class="sxs-lookup"><span data-stu-id="b78d7-142">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="b78d7-143">El método **ControlStream** funciona de cualquier manera.</span><span class="sxs-lookup"><span data-stu-id="b78d7-143">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="b78d7-144">En el caso de los PIN del puerto de vídeo, el método producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b78d7-144">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="b78d7-145">En ese caso, otro enfoque consiste en ocultar la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-145">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="b78d7-146">Consulte el gráfico para **IVideoWindow** y use el método [**\_ visible IVideoWindow::p UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar u ocultar la ventana.</span><span class="sxs-lookup"><span data-stu-id="b78d7-146">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="b78d7-147">Además, si llama a [**IVideoWindow::p UT \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor OAFALSE antes de ejecutar el gráfico, el filtro de representador de vídeo oculta la ventana hasta que especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="b78d7-147">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="b78d7-148">De forma predeterminada, el representador de vídeo muestra la ventana cuando se ejecuta el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b78d7-148">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="b78d7-149">Comentarios sobre el control de secuencias</span><span class="sxs-lookup"><span data-stu-id="b78d7-149">Remarks about Stream Control</span></span>

<span data-ttu-id="b78d7-150">El comportamiento predeterminado de un PIN es ofrecer ejemplos cuando se ejecuta el grafo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-150">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="b78d7-151">Por ejemplo, supongamos que llama a **ControlStream** con la captura de categoría de PIN, \_ \_ pero no con la \_ versión preliminar de categoría de PIN \_ .</span><span class="sxs-lookup"><span data-stu-id="b78d7-151">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="b78d7-152">Al ejecutar el gráfico, la secuencia de vista previa se ejecutará inmediatamente, mientras que la secuencia de captura se ejecutará en cualquier momento que se especifique en **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="b78d7-152">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="b78d7-153">Si está capturando más de una secuencia y las envía a un filtro MUX (por ejemplo, si va a capturar audio y vídeo en un archivo AVI), debe controlar ambos flujos en tándem.</span><span class="sxs-lookup"><span data-stu-id="b78d7-153">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="b78d7-154">De lo contrario, el filtro MUX podría bloquear la espera de un flujo, ya que intenta intercalar las dos secuencias.</span><span class="sxs-lookup"><span data-stu-id="b78d7-154">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="b78d7-155">Establezca las mismas horas de inicio y detención en todas las secuencias de captura antes de ejecutar el gráfico:</span><span class="sxs-lookup"><span data-stu-id="b78d7-155">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b78d7-156">Internamente, el método **ControlStream** usa la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , que se expone en las clavijas del filtro de captura, el filtro Smart Tee (si existe) y, posiblemente, el filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="b78d7-156">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="b78d7-157">Puede usar esta interfaz directamente, en lugar de llamar a **ControlStream**, aunque no hay ninguna ventaja concreta para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="b78d7-157">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b78d7-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b78d7-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b78d7-159">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b78d7-159">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



