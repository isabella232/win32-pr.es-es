---
description: Modo sin ventana de VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modo sin ventana de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360473"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="2715a-103">Modo sin ventana de VMR</span><span class="sxs-lookup"><span data-stu-id="2715a-103">VMR Windowless Mode</span></span>

<span data-ttu-id="2715a-104">El modo sin ventanas es la forma preferida para que las aplicaciones representen vídeo en una ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2715a-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="2715a-105">En el modo sin ventanas, el representador de mezcla de vídeo no carga su componente de administrador de Windows y, por lo tanto, no es compatible con las interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="2715a-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="2715a-106">En su lugar, la aplicación proporciona la ventana de reproducción y establece un rectángulo de destino en el área cliente para que la VMR dibuje el vídeo.</span><span class="sxs-lookup"><span data-stu-id="2715a-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="2715a-107">VMR usa un objeto Clipper de DirectDraw para asegurarse de que el vídeo se recorta en la ventana de la aplicación y no aparece en otras ventanas.</span><span class="sxs-lookup"><span data-stu-id="2715a-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="2715a-108">VMR no realiza la subclase de la ventana de la aplicación ni instala ningún enlace del sistema o proceso.</span><span class="sxs-lookup"><span data-stu-id="2715a-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="2715a-109">En el modo sin ventanas, la secuencia de eventos durante la conexión y la transición al estado de ejecución es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2715a-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="2715a-110">El filtro de nivel superior propone un tipo de medio, que la VMR acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="2715a-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="2715a-111">Si se acepta el tipo de medio, el archivo VMR llama al presentador del asignador para obtener una superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2715a-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="2715a-112">Si la superficie se crea correctamente, las clavijas Connect y la VMR están listas para realizar la transición al estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2715a-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="2715a-113">Cuando se ejecuta el gráfico de filtros, el descodificador llama a **getBuffer** para obtener un ejemplo multimedia del asignador.</span><span class="sxs-lookup"><span data-stu-id="2715a-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="2715a-114">VMR consulta al presentador del asignador para asegurarse de que la profundidad de píxeles, el tamaño del rectángulo y otros parámetros de su superficie de DirectDraw son compatibles con el vídeo entrante.</span><span class="sxs-lookup"><span data-stu-id="2715a-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="2715a-115">Si son compatibles, el VMR devuelve la superficie de DirectDraw al descodificador.</span><span class="sxs-lookup"><span data-stu-id="2715a-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="2715a-116">Una vez que el descodificador ha descodificado en la superficie, la unidad de sincronización principal de VMR valida las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2715a-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="2715a-117">Esta unidad bloquea la llamada de **recepción** hasta que llega el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="2715a-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="2715a-118">En ese momento, la VMR llama a **PresentImage** en el presentador del asignador, que presenta la superficie a la tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="2715a-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="2715a-119">En la ilustración siguiente se muestra el VMR en modo sin ventanas con varios flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="2715a-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR en modo sin ventanas](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="2715a-121">**Configuración de VMR-7 para el modo sin ventanas**</span><span class="sxs-lookup"><span data-stu-id="2715a-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="2715a-122">Para configurar VMR-7 para el modo sin ventanas, realice todos los pasos siguientes antes de conectar cualquiera de los pin de entrada de VMR:</span><span class="sxs-lookup"><span data-stu-id="2715a-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="2715a-123">Cree el filtro y agréguelo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="2715a-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="2715a-124">Llame al método [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con la \_ marca sin ventana de VMRMode.</span><span class="sxs-lookup"><span data-stu-id="2715a-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="2715a-125">Opcionalmente, configure la VMR para varios flujos de entrada mediante una llamada a [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="2715a-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="2715a-126">VMR crea un PIN de entrada para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="2715a-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="2715a-127">Use la interfaz [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para establecer el orden Z y otros parámetros para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2715a-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="2715a-128">Para obtener más información, consulte [VMR con varias secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="2715a-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="2715a-129">Si no llama a **SetNumberOfStreams**, el valor predeterminado de VMR-7 es un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="2715a-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="2715a-130">Una vez conectadas las clavijas de entrada, no se puede cambiar el número de clavijas.</span><span class="sxs-lookup"><span data-stu-id="2715a-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="2715a-131">Llame a [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar la ventana en la que aparecerá el vídeo representado.</span><span class="sxs-lookup"><span data-stu-id="2715a-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="2715a-132">Una vez completados estos pasos, puede conectar los pin de entrada del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="2715a-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="2715a-133">Hay varias maneras de compilar el gráfico, como la conexión directa de los pin, el uso de métodos de conexión inteligentes como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)o el uso del método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generador de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="2715a-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="2715a-134">Para obtener más información, vea [técnicas de Graph-Building generales](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="2715a-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="2715a-135">Para establecer la posición del vídeo dentro de la ventana de la aplicación, llame al método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="2715a-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="2715a-136">El método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) devuelve el tamaño de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="2715a-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="2715a-137">Durante la reproducción, la aplicación debe notificar a la VMR los siguientes mensajes de Windows:</span><span class="sxs-lookup"><span data-stu-id="2715a-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="2715a-138">WM \_ Paint: llame a [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para volver a dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="2715a-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="2715a-139">WM \_ DISPLAYCHANGE: llame a [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="2715a-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="2715a-140">La VMR toma las medidas necesarias para mostrar el vídeo con la nueva resolución o profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="2715a-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="2715a-141">\_Tamaño de WM: vuelva a calcular la posición del vídeo y llame de nuevo a [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) si es necesario.</span><span class="sxs-lookup"><span data-stu-id="2715a-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="2715a-142">Las aplicaciones MFC deben definir un controlador de mensajes ERASEBKGND de WM vacío \_ o el área de presentación de vídeo no volverá a dibujarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="2715a-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="2715a-143">**Configuración de VMR-9 para el modo sin ventanas**</span><span class="sxs-lookup"><span data-stu-id="2715a-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="2715a-144">Para configurar VMR-9 para el modo sin ventanas, siga los pasos descritos en VMR-7 para el modo sin ventanas, pero use las interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) y [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="2715a-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="2715a-145">La única diferencia significativa es que VMR-9 crea cuatro clavijas de entrada de forma predeterminada, en lugar de un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="2715a-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="2715a-146">Por lo tanto, solo tiene que llamar a **SetNumberOfStreams** si está mezclando más de cuatro secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2715a-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="2715a-147">**Código de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2715a-147">**Example Code**</span></span>

<span data-ttu-id="2715a-148">En el código siguiente se muestra cómo crear un filtro VMR-7, agregarlo al gráfico de filtros de DirectShow y, a continuación, colocar el VMR en el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="2715a-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="2715a-149">En el caso de VMR-9, use CLSID \_ VideoMixingRenderer9 en **CoCreateInstance** y las interfaces de VMR-9 correspondientes.</span><span class="sxs-lookup"><span data-stu-id="2715a-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2715a-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2715a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2715a-151">Usar el modo sin ventanas</span><span class="sxs-lookup"><span data-stu-id="2715a-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



