---
description: Ver teletexto estándar del mundo
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Ver teletexto estándar del mundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360474"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="404ac-103">Ver teletexto estándar del mundo</span><span class="sxs-lookup"><span data-stu-id="404ac-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="404ac-104">Esta funcionalidad se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="404ac-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="404ac-105">Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="404ac-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="404ac-106">El teletexto estándar universal (elemento WST) está codificado en el intervalo de blanking vertical (VBI) de la señal de televisión analógica.</span><span class="sxs-lookup"><span data-stu-id="404ac-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="404ac-107">El gráfico de filtro para obtener una vista previa del teletexto es similar al gráfico que se usa para ver los subtítulos cerrados.</span><span class="sxs-lookup"><span data-stu-id="404ac-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="404ac-108">En el siguiente diagrama se ilustra este gráfico.</span><span class="sxs-lookup"><span data-stu-id="404ac-108">The following diagram illustrates this graph.</span></span>

![gráfico de vista previa de elemento WST](images/vidcap10.png)

<span data-ttu-id="404ac-110">En este gráfico se usan los siguientes filtros para la visualización de elemento WST:</span><span class="sxs-lookup"><span data-stu-id="404ac-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="404ac-111">[Convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="404ac-112">Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal.</span><span class="sxs-lookup"><span data-stu-id="404ac-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="404ac-113">[Códec elemento WST](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="404ac-114">Descodifica los datos de teletexto de los ejemplos de VBI.</span><span class="sxs-lookup"><span data-stu-id="404ac-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="404ac-115">[Descodificador de elemento WST](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="404ac-116">Traduce los datos de teletexto y dibuja el texto en mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="404ac-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="404ac-117">El filtro de nivel inferior (en este caso, el mezclador de superposición) superpone los mapas de bits al vídeo.</span><span class="sxs-lookup"><span data-stu-id="404ac-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="404ac-118">El método **RenderStream** del generador de gráficos de captura no admite directamente los filtros elemento WST, por lo que la aplicación debe realizar algún trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="404ac-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="404ac-119">Agregue el filtro de mezclador de superposición al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="404ac-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="404ac-120">En el código siguiente se usa la función AddFilterByCLSID que se describe en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="404ac-121">(AddFilterByCLSID no es una API de DirectShow).</span><span class="sxs-lookup"><span data-stu-id="404ac-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="404ac-122">Conecte el PIN de vista previa al filtro de representador de vídeo a través del mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="404ac-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="404ac-123">Puede usar el método **RenderStream** , como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="404ac-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="404ac-124">Agregue el filtro de convertidor Tee/Sink-to-Sink al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="404ac-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="404ac-125">En el código siguiente se usa la función CreateKernelFilter que se describe en [crear Kernel-Mode filtros](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="404ac-126">(CreateKernelFilter no es una API de DirectShow).</span><span class="sxs-lookup"><span data-stu-id="404ac-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="404ac-127">Agregue el filtro de códec elemento WST al gráfico de filtros:</span><span class="sxs-lookup"><span data-stu-id="404ac-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="404ac-128">Llame a **RenderStream** para conectar el PIN VBI del filtro de captura al convertidor Tee/Sink-to-Sink y el convertidor Tee/Sink-to-Sink al filtro de códec elemento WST:</span><span class="sxs-lookup"><span data-stu-id="404ac-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="404ac-129">Vuelva a llamar a **RenderStream** para conectar el filtro de códec elemento WST al mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="404ac-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="404ac-130">El filtro del descodificador de elemento WST se incorpora automáticamente al gráfico.</span><span class="sxs-lookup"><span data-stu-id="404ac-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="404ac-131">Recuerde liberar todas las interfaces de filtro.</span><span class="sxs-lookup"><span data-stu-id="404ac-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="404ac-132">Actualmente, el filtro del descodificador de elemento WST no admite conexiones al filtro de representador de mezcla de vídeo (VMR).</span><span class="sxs-lookup"><span data-stu-id="404ac-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="404ac-133">Por lo tanto, debe usar el filtro de representador de vídeo heredado para ver el teletexto.</span><span class="sxs-lookup"><span data-stu-id="404ac-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="404ac-134">Si el filtro de captura tiene un PIN de puerto de vídeo VBI (PIN \_ CATEGPORY \_ videopuerto \_ VBI), conéctelo al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="404ac-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="404ac-135">De lo contrario, el gráfico no se ejecutará correctamente.</span><span class="sxs-lookup"><span data-stu-id="404ac-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="404ac-136">En el ejemplo de código siguiente se usa la función AddFilterByCLSID, que se describe en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)y la función FindPinByCategory, que se describe en [trabajar con categorías de PIN](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="404ac-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="404ac-137">(Ninguna de las funciones es una API de DirectShow).</span><span class="sxs-lookup"><span data-stu-id="404ac-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="404ac-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="404ac-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="404ac-139">Subtítulos y teletexto</span><span class="sxs-lookup"><span data-stu-id="404ac-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



