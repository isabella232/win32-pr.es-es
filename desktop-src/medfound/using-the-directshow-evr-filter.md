---
description: Usar el filtro EVR de DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Usar el filtro EVR de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687306"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="e7e60-103">Usar el filtro EVR de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7e60-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="e7e60-104">Para crear el filtro de representador de vídeo mejorado (EVR), llame a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e7e60-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="e7e60-105">El CLSID es CLSID \_ EnhancedVideoRenderer, definido en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="e7e60-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="e7e60-106">No es necesario llamar a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para usar el filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="e7e60-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="e7e60-107">Para obtener más información sobre el uso del filtro EVR en una aplicación de DirectShow, vea [reproducción de audio y vídeo en DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e7e60-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="e7e60-108">El filtro EVR se inicia con un PIN de entrada, que corresponde a la secuencia de referencia.</span><span class="sxs-lookup"><span data-stu-id="e7e60-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="e7e60-109">Para agregar PIN para subflujos, consulte el filtro de la interfaz [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) y llame a [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="e7e60-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="e7e60-110">Llame a este método antes de conectar cualquier clavija de entrada.</span><span class="sxs-lookup"><span data-stu-id="e7e60-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="e7e60-111">El pin 0 siempre es el flujo de referencia.</span><span class="sxs-lookup"><span data-stu-id="e7e60-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="e7e60-112">Conecte este PIN antes de cualquier otro PIN, ya que el formato del flujo de referencia puede limitar los formatos de subsecuencia que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="e7e60-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="e7e60-113">Antes de iniciar el gráfico, establezca la ventana de recorte de vídeo y el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e60-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="e7e60-114">Para obtener más información, vea [usar los controles de presentación de vídeo](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e7e60-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="e7e60-115">A diferencia del representador de mezcla de vídeo (VMR), EVR no tiene modos operativos (windowed, Windowless, etc.).</span><span class="sxs-lookup"><span data-stu-id="e7e60-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="e7e60-116">En concreto:</span><span class="sxs-lookup"><span data-stu-id="e7e60-116">In particular:</span></span>

-   <span data-ttu-id="e7e60-117">EVR no admite el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="e7e60-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="e7e60-118">La aplicación debe proporcionar la ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="e7e60-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="e7e60-119">EVR no tiene un modo sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e7e60-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="e7e60-120">Para reemplazar el presentador predeterminado, llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="e7e60-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="e7e60-121">El EVR no tiene un modo de mezcla.</span><span class="sxs-lookup"><span data-stu-id="e7e60-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="e7e60-122">EVR siempre crea el mezclador.</span><span class="sxs-lookup"><span data-stu-id="e7e60-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="e7e60-123">Si tiene un flujo de entrada, no es necesario llamar a [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para obligar a EVR a usar el mezclador.</span><span class="sxs-lookup"><span data-stu-id="e7e60-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="e7e60-124">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="e7e60-124">Filter Interfaces</span></span>

<span data-ttu-id="e7e60-125">El filtro EVR expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="e7e60-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="e7e60-126">Algunas de estas interfaces se documentan en el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e7e60-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="e7e60-127">Use **QueryInterface** para recuperar punteros a estas interfaces:</span><span class="sxs-lookup"><span data-stu-id="e7e60-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="e7e60-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="e7e60-131">**IEVRFilterConfig**</span><span class="sxs-lookup"><span data-stu-id="e7e60-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="e7e60-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="e7e60-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="e7e60-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="e7e60-135">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="e7e60-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="e7e60-136">**IMFVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e7e60-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="e7e60-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="e7e60-137">**IPersistStream**</span></span>
-   <span data-ttu-id="e7e60-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="e7e60-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="e7e60-141">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="e7e60-141">Input Pin Interfaces</span></span>

<span data-ttu-id="e7e60-142">Los pin de entrada del filtro EVR exponen las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7e60-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="e7e60-143">Use **QueryInterface** para recuperar punteros a estas interfaces:</span><span class="sxs-lookup"><span data-stu-id="e7e60-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="e7e60-144">**IEVRVideoStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e7e60-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="e7e60-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="e7e60-146">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="e7e60-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="e7e60-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="e7e60-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e7e60-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="e7e60-149">Además, puede usar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para recuperar la siguiente interfaz:</span><span class="sxs-lookup"><span data-stu-id="e7e60-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="e7e60-150">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e7e60-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="e7e60-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7e60-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e60-152">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7e60-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="e7e60-153">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="e7e60-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
