---
description: Ver subtítulos (CC)
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Ver subtítulos (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569712"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="261f9-103">Ver subtítulos (CC)</span><span class="sxs-lookup"><span data-stu-id="261f9-103">Viewing Closed Captions</span></span>

<span data-ttu-id="261f9-104">Para admitir subtítulos (CC) en televisión analógica, el filtro de captura expone un PIN que proporciona datos de subtítulos o de subtítulos cerrados.</span><span class="sxs-lookup"><span data-stu-id="261f9-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="261f9-105">El PIN tendrá una de las siguientes categorías de PIN:</span><span class="sxs-lookup"><span data-stu-id="261f9-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="261f9-106">PIN de VBI ( \_ categoría de PIN \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="261f9-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="261f9-107">Proporciona una secuencia de ejemplos de perfiles de onda de VBI.</span><span class="sxs-lookup"><span data-stu-id="261f9-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="261f9-108">Estos se pasan a un filtro de descodificador que extrae los datos de subtítulos.</span><span class="sxs-lookup"><span data-stu-id="261f9-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="261f9-109">PIN CC (categoría de PIN \_ \_ CC).</span><span class="sxs-lookup"><span data-stu-id="261f9-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="261f9-110">Proporciona pares de bytes de subtítulos cerrados, extraídos de los datos de la línea 21.</span><span class="sxs-lookup"><span data-stu-id="261f9-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="261f9-111">División de hardware de la segmentación CC ( \_ captura de CC de vídeo PINNAME \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="261f9-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="261f9-112">Para obtener una vista previa de los subtítulos cerrados, llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoría de PIN de VBI y, si se produce un error, vuelva a llamarlo con la categoría CC.</span><span class="sxs-lookup"><span data-stu-id="261f9-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="261f9-113">En el diagrama siguiente se muestra un gráfico de filtros típico para mostrar subtítulos cerrados.</span><span class="sxs-lookup"><span data-stu-id="261f9-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![gráfico de vista previa de subtítulos (CC)](images/vidcap08.png)

<span data-ttu-id="261f9-115">En este gráfico se usan los siguientes filtros para la presentación de subtítulos:</span><span class="sxs-lookup"><span data-stu-id="261f9-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="261f9-116">[Convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="261f9-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="261f9-117">Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal.</span><span class="sxs-lookup"><span data-stu-id="261f9-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="261f9-118">Microsoft proporciona códecs VBI para el título cerrado, NABTS y teletexto universal estándar (elemento WST).</span><span class="sxs-lookup"><span data-stu-id="261f9-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="261f9-119">[Descodificador de CC](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="261f9-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="261f9-120">Descodifica los datos de CC de las forma de onda VBI muestreadas proporcionadas por el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="261f9-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="261f9-121">[Descodificador de línea 21](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="261f9-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="261f9-122">Traduce los pares de bytes de CC y dibuja el texto de la leyenda en mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="261f9-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="261f9-123">El filtro de nivel inferior (en este caso, el mezclador de superposición) superpone los mapas de bits al vídeo.</span><span class="sxs-lookup"><span data-stu-id="261f9-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="261f9-124">El método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generador de gráficos de captura agrega estos filtros automáticamente.</span><span class="sxs-lookup"><span data-stu-id="261f9-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="261f9-125">Si el filtro de captura tiene un PIN de CC en lugar de un PIN de VBI, el PIN de CC se conecta directamente al filtro de descodificador de línea 21.</span><span class="sxs-lookup"><span data-stu-id="261f9-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="261f9-126">Si usa el filtro de representador de mezcla de vídeo (VMR) para la representación, use el filtro de descodificador de línea 21 2.</span><span class="sxs-lookup"><span data-stu-id="261f9-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="261f9-127">Este filtro tiene la misma funcionalidad que el descodificador de línea 21, pero el CLSID es CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="261f9-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="261f9-128">El filtro del descodificador de CC se quitó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="261f9-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="261f9-129">Las nuevas aplicaciones deben usar el filtro VBICodec, que se documenta en la documentación de las tecnologías de Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="261f9-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="261f9-130">Si el dispositivo de captura usa un puerto de vídeo, el filtro de captura podría tener un PIN de puerto de vídeo VBI (categoría de PIN de \_ \_ videopuerto \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="261f9-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="261f9-131">Este pin debe estar conectado al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) , que asigna superficies para almacenar los datos de VBI capturados.</span><span class="sxs-lookup"><span data-stu-id="261f9-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="261f9-132">El método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega este filtro si es necesario.</span><span class="sxs-lookup"><span data-stu-id="261f9-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="261f9-133">En el diagrama siguiente se muestra un gráfico de filtros con el asignador de superficie de VBI.</span><span class="sxs-lookup"><span data-stu-id="261f9-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![gráfico de vista previa de subtítulos (CC) con asignador de superficie de VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="261f9-135">Habilitar y deshabilitar los títulos</span><span class="sxs-lookup"><span data-stu-id="261f9-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="261f9-136">Para controlar la presentación de subtítulos, use la interfaz [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) en el filtro del descodificador line 21.</span><span class="sxs-lookup"><span data-stu-id="261f9-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="261f9-137">Por ejemplo, puede desactivar la presentación de subtítulos mediante el método [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="261f9-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="261f9-138">En este ejemplo se usa el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar la interfaz [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) .</span><span class="sxs-lookup"><span data-stu-id="261f9-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="261f9-139">El primer parámetro de **FindInterface** es **&look \_ downstream \_ Only**, que especifica que se busque downstream desde el filtro de captura (*pCap*).</span><span class="sxs-lookup"><span data-stu-id="261f9-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="261f9-140">Captura de mapas de bits de subtítulos cerrados</span><span class="sxs-lookup"><span data-stu-id="261f9-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="261f9-141">Puede capturar los mapas de bits de los títulos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="261f9-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="261f9-142">Para ello, agregue la sección de escritura de archivos del gráfico de filtros, como se describe en [capturar vídeo en un archivo](capturing-video-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="261f9-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="261f9-143">A continuación, represente el PIN de CC o VBI en el filtro MUX:</span><span class="sxs-lookup"><span data-stu-id="261f9-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="261f9-144">Si también va a capturar el vídeo, se creará un archivo con dos secuencias de vídeo independientes.</span><span class="sxs-lookup"><span data-stu-id="261f9-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="261f9-145">No capturará vídeo con títulos superpuestos encima de la imagen.</span><span class="sxs-lookup"><span data-stu-id="261f9-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="261f9-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="261f9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="261f9-147">Subtítulos y teletexto</span><span class="sxs-lookup"><span data-stu-id="261f9-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



