---
description: Obtener una vista previa del vídeo
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Obtener una vista previa del vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563773"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="1d4b9-103">Obtener una vista previa del vídeo (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="1d4b9-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="1d4b9-104">Para compilar un gráfico de vista previa de vídeo, llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1d4b9-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="1d4b9-105">En este ejemplo se da por supuesto lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d4b9-105">This example assumes the following:</span></span>

-   <span data-ttu-id="1d4b9-106">se inicializó *pBuild* , tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="1d4b9-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="1d4b9-107">para inicializar *pCap* , se crea una instancia del filtro de captura y se agrega al gráfico de filtros, como se describe en [seleccionar un dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="1d4b9-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="1d4b9-108">El primer parámetro del método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica una categoría de PIN; para un gráfico de vista previa, use **PIN \_ categoría \_ Preview**.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="1d4b9-109">El segundo parámetro especifica un tipo de medio, como un GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="1d4b9-110">Para vídeo, use **el \_ vídeo MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="1d4b9-111">Los dispositivos DV proporcionan audio y vídeo intercalados, para los que el tipo de medio es de tipo medio **\_ intercalado**.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="1d4b9-112">(Para obtener más información acerca de la captura de DV, consulte [vídeo digital en DirectShow](digital-video-in-directshow.md)).</span><span class="sxs-lookup"><span data-stu-id="1d4b9-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="1d4b9-113">El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="1d4b9-114">Los dos parámetros siguientes no son necesarios en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="1d4b9-115">Se usan para especificar filtros adicionales que podrían ser necesarios para representar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="1d4b9-116">Al establecer el último parámetro en **null** , el generador de gráficos de captura selecciona un representador predeterminado para la secuencia, en función del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="1d4b9-117">En el caso de vídeo, el generador de gráficos de captura siempre usa el filtro de [representador de vídeo](video-renderer-filter.md) como representador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="1d4b9-118">En Windows XP y versiones posteriores, aunque el representador de mezcla de vídeo (VMR) es el representador de vídeo predeterminado para los métodos de [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , no es el representador predeterminado para el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="1d4b9-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="1d4b9-119">En cualquier plataforma, el generador de gráficos de captura siempre usa el filtro de representador de vídeo anterior, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="1d4b9-120">Aunque la categoría PIN se proporciona como **\_ \_ vista previa de categoría PIN**, no importa si el filtro tiene realmente un PIN de vista previa; podría tener un PIN de puerto de vídeo o simplemente un PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="1d4b9-121">En cualquier caso, el generador de gráficos de captura crea automáticamente el gráfico correcto.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="1d4b9-122">En el diagrama siguiente se muestra el gráfico más sencillo posible para obtener una vista previa del vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![gráfico de vista previa de vídeo](images/vidcap01.png)

<span data-ttu-id="1d4b9-124">En este diagrama, el filtro de captura tiene un PIN de vista previa, que se conecta directamente al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="1d4b9-125">Si el filtro de captura solo tiene un PIN de captura, el generador de gráficos de captura inserta un filtro de forma [inteligente](smart-tee-filter.md) , que divide la secuencia en una secuencia de captura y una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="1d4b9-126">Esto se describe con más detalle en [combinación de captura de vídeo y vista previa](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="1d4b9-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="1d4b9-127">En algunos casos, el flujo de vídeo debe atravesar el filtro de mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="1d4b9-128">Si es así, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo agrega automáticamente al gráfico.</span><span class="sxs-lookup"><span data-stu-id="1d4b9-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d4b9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d4b9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d4b9-130">Combinación de captura de vídeo y vista previa</span><span class="sxs-lookup"><span data-stu-id="1d4b9-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="1d4b9-131">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="1d4b9-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



