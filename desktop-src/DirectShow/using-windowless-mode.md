---
description: Usar el modo sin ventanas
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Usar el modo sin ventanas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911066"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="333dc-103">Usar el modo sin ventanas</span><span class="sxs-lookup"><span data-stu-id="333dc-103">Using Windowless Mode</span></span>

<span data-ttu-id="333dc-104">Tanto el [filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) como el [filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) admiten el *modo sin ventanas*, que representa una mejora importante sobre la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="333dc-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="333dc-105">En este tema se describen las diferencias entre el modo sin ventanas y el modo de ventana, y cómo usar el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="333dc-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="333dc-106">Para mantener la compatibilidad con versiones anteriores de las aplicaciones existentes, la VMR tiene como valor predeterminado el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="333dc-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="333dc-107">En el modo de ventana, el representador crea su propia ventana para mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="333dc-108">Normalmente, la aplicación establece la ventana de vídeo para que sea un elemento secundario de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="333dc-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="333dc-109">Sin embargo, la existencia de una ventana de vídeo independiente provoca algunos problemas:</span><span class="sxs-lookup"><span data-stu-id="333dc-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="333dc-110">Lo más importante es que existe la posibilidad de que se produzcan interbloqueos si se envían mensajes de ventana entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="333dc-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="333dc-111">Filter Graph Manager debe reenviar determinados mensajes de ventana, como WM \_ Paint, al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="333dc-112">La aplicación debe usar la implementación del administrador de gráficos de filtro de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (y no la del representador de vídeo), por lo que el administrador de gráficos de filtro mantiene el estado interno correcto.</span><span class="sxs-lookup"><span data-stu-id="333dc-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="333dc-113">Para recibir eventos del mouse o del teclado desde la ventana de vídeo, la aplicación debe establecer una *purga de mensajes*, lo que hará que la ventana de vídeo reenvíe estos mensajes a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="333dc-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="333dc-114">Para evitar problemas de recorte, la ventana de vídeo debe tener los estilos de ventana correctos.</span><span class="sxs-lookup"><span data-stu-id="333dc-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="333dc-115">El modo sin ventanas evita estos problemas al hacer que la VMR dibuje directamente en el área de cliente de la ventana de la aplicación, usando DirectDraw para recortar el rectángulo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="333dc-116">El modo sin ventanas reduce significativamente la posibilidad de que se produzcan interbloqueos.</span><span class="sxs-lookup"><span data-stu-id="333dc-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="333dc-117">Además, la aplicación no tiene que establecer la ventana propietaria ni los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="333dc-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="333dc-118">De hecho, cuando el VMR está en modo sin ventanas, ni siquiera expone la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , que ya no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="333dc-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="333dc-119">Para usar el modo sin ventanas, debe configurar explícitamente la VMR.</span><span class="sxs-lookup"><span data-stu-id="333dc-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="333dc-120">Sin embargo, observará que es más flexible y más fácil de usar que el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="333dc-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="333dc-121">El filtro VMR-7 y el filtro VMR-9 exponen interfaces diferentes, pero los pasos son equivalentes para cada uno.</span><span class="sxs-lookup"><span data-stu-id="333dc-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="333dc-122">Configurar VMR para el modo sin ventanas</span><span class="sxs-lookup"><span data-stu-id="333dc-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="333dc-123">Para invalidar el comportamiento predeterminado de la VMR, configure el VMR antes de compilar el gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="333dc-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="333dc-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="333dc-124">**VMR-7**</span></span>

1.  <span data-ttu-id="333dc-125">Cree el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="333dc-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="333dc-126">Cree el VMR-7 y agréguelo al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="333dc-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="333dc-127">Llame a [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) en la VMR-7 con la marca **\_ sin ventana de VMRMode** .</span><span class="sxs-lookup"><span data-stu-id="333dc-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="333dc-128">Consulte VMR-7 para la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="333dc-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="333dc-129">Llame a [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) en VMR-7.</span><span class="sxs-lookup"><span data-stu-id="333dc-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="333dc-130">Especifique un identificador para la ventana en la que debe aparecer el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="333dc-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="333dc-131">**VMR-9**</span></span>

1.  <span data-ttu-id="333dc-132">Cree el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="333dc-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="333dc-133">Cree el VMR-9 y agréguelo al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="333dc-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="333dc-134">Llame a [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) en VMR-9 con la **marca \_ sin ventana de VMR9Mode** .</span><span class="sxs-lookup"><span data-stu-id="333dc-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="333dc-135">Consulte VMR-9 para la interfaz [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="333dc-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="333dc-136">Llame a [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) en VMR-9.</span><span class="sxs-lookup"><span data-stu-id="333dc-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="333dc-137">Especifique un identificador para la ventana en la que debe aparecer el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="333dc-138">Ahora compile el resto del gráfico de filtro llamando a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) u otros métodos de creación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="333dc-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="333dc-139">El administrador de gráficos de filtro utiliza automáticamente la instancia de VMR que agregó al gráfico.</span><span class="sxs-lookup"><span data-stu-id="333dc-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="333dc-140">(Para más información sobre por qué sucede esto, consulte [conexión inteligente](intelligent-connect.md)).</span><span class="sxs-lookup"><span data-stu-id="333dc-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="333dc-141">En el código siguiente se muestra una función auxiliar que crea el VMR-7, lo agrega al gráfico y establece el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="333dc-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="333dc-142">Esta función supone que solo muestra un flujo de vídeo y no está mezclando un mapa de bits estático sobre el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="333dc-143">Para obtener más información, consulte [modo sin ventanas de VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="333dc-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="333dc-144">Llamaría a esta función como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="333dc-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="333dc-145">Colocar el vídeo</span><span class="sxs-lookup"><span data-stu-id="333dc-145">Position the Video</span></span>

<span data-ttu-id="333dc-146">Después de configurar la VMR, el siguiente paso es establecer la posición del vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="333dc-147">Hay dos rectángulos que se deben tener en cuenta: el rectángulo de *origen* y el de *destino* .</span><span class="sxs-lookup"><span data-stu-id="333dc-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="333dc-148">El rectángulo de origen define qué parte del vídeo se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="333dc-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="333dc-149">El rectángulo de destino especifica la región del área de cliente de la ventana que contendrá el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="333dc-150">VMR recorta la imagen de vídeo con el rectángulo de origen y ajusta la imagen recortada para ajustarse al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="333dc-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="333dc-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="333dc-151">**VMR-7**</span></span>

1.  <span data-ttu-id="333dc-152">Llame al método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para especificar ambos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="333dc-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="333dc-153">El rectángulo de origen debe ser igual o menor que el tamaño de vídeo nativo; puede usar el método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) para obtener el tamaño de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="333dc-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="333dc-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="333dc-154">**VMR-9**</span></span>

1.  <span data-ttu-id="333dc-155">Llame al método [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para especificar ambos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="333dc-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="333dc-156">El rectángulo de origen debe ser igual o menor que el tamaño de vídeo nativo; puede usar el método [**IVMRWindowlessControl9:: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) para obtener el tamaño de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="333dc-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="333dc-157">Por ejemplo, el código siguiente establece los rectángulos de origen y de destino para VMR-7.</span><span class="sxs-lookup"><span data-stu-id="333dc-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="333dc-158">Establece el rectángulo de origen igual a toda la imagen de vídeo y el rectángulo de destino es igual a todo el área cliente de la ventana:</span><span class="sxs-lookup"><span data-stu-id="333dc-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="333dc-159">Si desea que el vídeo ocupe una parte más pequeña del área cliente, modifique el parámetro *rcDest* .</span><span class="sxs-lookup"><span data-stu-id="333dc-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="333dc-160">Si desea recortar la imagen de vídeo, modifique el parámetro *rcSrc* .</span><span class="sxs-lookup"><span data-stu-id="333dc-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="333dc-161">Controlar mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="333dc-161">Handle Window Messages</span></span>

<span data-ttu-id="333dc-162">Dado que VMR no tiene su propia ventana, se debe notificar si es necesario volver a dibujar o cambiar el tamaño del vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="333dc-163">Para responder a los siguientes mensajes de ventana, llame a los métodos VMR enumerados.</span><span class="sxs-lookup"><span data-stu-id="333dc-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="333dc-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="333dc-164">**VMR-7**</span></span>

1.  <span data-ttu-id="333dc-165">[**WM \_ PINTAR**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="333dc-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="333dc-166">Llame a [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="333dc-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="333dc-167">Este método hace que VMR-7 Vuelva a dibujar el fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="333dc-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="333dc-168">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): llame a [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="333dc-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="333dc-169">Este método notifica a VMR-7 que el vídeo debe mostrarse con una nueva resolución o profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="333dc-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="333dc-170">[**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): vuelva a calcular la posición del vídeo y llame a [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para actualizar la posición, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="333dc-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="333dc-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="333dc-171">**VMR-9**</span></span>

1.  <span data-ttu-id="333dc-172">[**WM \_ PINTAR**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="333dc-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="333dc-173">Llame a [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="333dc-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="333dc-174">Este método hace que VMR-9 vuelva a dibujar el fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="333dc-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="333dc-175">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): llame a [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="333dc-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="333dc-176">Este método notifica a VMR-9 que el vídeo debe mostrarse con una nueva resolución o profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="333dc-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="333dc-177">[**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): vuelva a calcular la posición del vídeo y llame a [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para actualizar la posición, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="333dc-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="333dc-178">El controlador predeterminado para el mensaje de [**\_ WINDOWPOSCHANGED de WM**](../winmsg/wm-windowposchanged.md) envía un mensaje de [**\_ tamaño de WM**](../winmsg/wm-size.md) .</span><span class="sxs-lookup"><span data-stu-id="333dc-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="333dc-179">Pero si la aplicación intercepta **WM \_ WINDOWPOSCHANGED** y no lo pasa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), debe llamar a **SetVideoPosition** en el controlador de **WM \_ WINDOWPOSCHANGED** , además del controlador de **\_ tamaño de WM** .</span><span class="sxs-lookup"><span data-stu-id="333dc-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="333dc-180">En el ejemplo siguiente se muestra un controlador de mensajes de [**\_ Paint de WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="333dc-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="333dc-181">Pinta una región definida por el rectángulo del cliente menos el rectángulo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="333dc-182">No dibuje en el rectángulo de vídeo, ya que el VMR dibujará sobre él, lo que provocará parpadeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="333dc-183">Por la misma razón, no establezca un pincel de fondo en la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="333dc-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="333dc-184">Aunque debe responder a los mensajes de [**WM \_ Paint**](../gdi/wm-paint.md) , no es necesario realizar ninguna acción entre los mensajes de **WM \_ Paint** para actualizar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="333dc-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="333dc-185">Como se muestra en este ejemplo, el modo sin ventanas le permite tratar la imagen de vídeo simplemente como una región de dibujo propio en la ventana.</span><span class="sxs-lookup"><span data-stu-id="333dc-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="333dc-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="333dc-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="333dc-187">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="333dc-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="333dc-188">Representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="333dc-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
