---
description: En este ejemplo se crea un gráfico de vista previa de vídeo mediante el método ICaptureGraphBuilder2::RenderStream en DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Vista previa de vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406898"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="464b6-103">Vista previa de vídeo (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="464b6-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="464b6-104">Para crear un gráfico de vista previa de vídeo, llame al método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="464b6-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="464b6-105">En este ejemplo se da por supuesto lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="464b6-105">This example assumes the following:</span></span>

-   <span data-ttu-id="464b6-106">*pBuild* se inicializó, como se describe en [Acerca del Generador de gráficos de captura.](about-the-capture-graph-builder.md)</span><span class="sxs-lookup"><span data-stu-id="464b6-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="464b6-107">*pCap* se inicializó mediante la creación de una instancia del filtro de captura y su adición al gráfico de filtros, como se describe en [Selección de un dispositivo de captura.](selecting-a-capture-device.md)</span><span class="sxs-lookup"><span data-stu-id="464b6-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="464b6-108">El primer parámetro del método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica una categoría pin; Para un gráfico de vista previa, use **PIN \_ CATEGORY \_ PREVIEW**.</span><span class="sxs-lookup"><span data-stu-id="464b6-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="464b6-109">El segundo parámetro especifica un tipo de medio, como un GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="464b6-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="464b6-110">En el caso del vídeo, use **MEDIATYPE \_ Video**.</span><span class="sxs-lookup"><span data-stu-id="464b6-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="464b6-111">Los dispositivos DV proporcionan audio y vídeo intercalados, para los que el tipo de medio **es MEDIATYPE \_ intercalado.**</span><span class="sxs-lookup"><span data-stu-id="464b6-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="464b6-112">(Para obtener más información sobre la captura de DV, vea [Vídeo digital en DirectShow).](digital-video-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="464b6-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="464b6-113">El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="464b6-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="464b6-114">Los dos parámetros siguientes no son necesarios en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="464b6-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="464b6-115">Se usan para especificar filtros adicionales que podrían ser necesarios para representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="464b6-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="464b6-116">Al establecer el último parámetro en **NULL,** Capture Graph Builder selecciona un representador predeterminado para la secuencia, en función del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="464b6-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="464b6-117">En el caso del vídeo, Capture Graph Builder siempre usa el filtro [Representador de](video-renderer-filter.md) vídeo como representador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="464b6-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="464b6-118">En Windows XP y versiones posteriores, aunque el representador de mezcla de vídeo (VMR) es el representador de vídeo predeterminado para los métodos [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) no es el representador predeterminado para el [**método RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)</span><span class="sxs-lookup"><span data-stu-id="464b6-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="464b6-119">En cualquier plataforma, Capture Graph Builder siempre usa el filtro De representador de vídeo antiguo, a menos que especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="464b6-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="464b6-120">Aunque la categoría pin se proporciona como **PIN \_ CATEGORY \_ PREVIEW**, no importa si el filtro tiene realmente un pin de vista previa; podría tener un pin de puerto de vídeo o simplemente un pin de captura.</span><span class="sxs-lookup"><span data-stu-id="464b6-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="464b6-121">En cualquier caso, Capture Graph Builder compila automáticamente el gráfico correcto.</span><span class="sxs-lookup"><span data-stu-id="464b6-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="464b6-122">En el diagrama siguiente se muestra el gráfico más sencillo posible para obtener una vista previa del vídeo.</span><span class="sxs-lookup"><span data-stu-id="464b6-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![gráfico de vista previa de vídeo](images/vidcap01.png)

<span data-ttu-id="464b6-124">En este diagrama, el filtro de captura tiene un pin de vista previa, que se conecta directamente al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="464b6-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="464b6-125">Si el filtro de captura solo tiene un pin de captura, Capture Graph Builder inserta un filtro [smart tee,](smart-tee-filter.md) que divide la secuencia en una secuencia de captura y una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="464b6-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="464b6-126">Esto se describe con más detalle en [Combinación de captura de vídeo y versión preliminar.](combining-video-capture-and-preview.md)</span><span class="sxs-lookup"><span data-stu-id="464b6-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="464b6-127">En algunos casos, la secuencia de vídeo debe pasar por el filtro Mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="464b6-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="464b6-128">Si es así, [**el método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo agrega al gráfico automáticamente.</span><span class="sxs-lookup"><span data-stu-id="464b6-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="464b6-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="464b6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="464b6-130">Combinación de captura de vídeo y versión preliminar</span><span class="sxs-lookup"><span data-stu-id="464b6-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="464b6-131">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="464b6-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



