---
description: Capturar un archivo de tipo 1 DV
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturar un archivo de tipo 1 DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556445"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="ca3e2-103">Capturar un archivo de tipo 1 DV</span><span class="sxs-lookup"><span data-stu-id="ca3e2-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="ca3e2-104">Un archivo AVI de tipo 1 digital contiene una única secuencia intercalada.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="ca3e2-105">Para capturar un archivo de tipo 1 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![captura de tipo 1 con vista previa](images/dv1-cap.png)

<span data-ttu-id="ca3e2-107">Los filtros de este grafo incluyen:</span><span class="sxs-lookup"><span data-stu-id="ca3e2-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="ca3e2-108">Este [filtro divide el DV](smart-tee-filter.md) intercalado en una secuencia de captura y en una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="ca3e2-109">Ambas secuencias contienen los mismos datos intercalados.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="ca3e2-110">[AVI MUX](avi-mux-filter.md) y el [escritor de archivos](file-writer-filter.md) escriben el flujo intercalado en el disco.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="ca3e2-111">El [divisor DV](dv-splitter-filter.md) divide el flujo intercalado en una secuencia de vídeo DV y en una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="ca3e2-112">Ambos flujos se rendererd para la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="ca3e2-113">El [descodificador de vídeo DV](dv-video-decoder-filter.md) descodifica el flujo de vídeo DV para la vista previa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="ca3e2-114">Compile este gráfico como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ca3e2-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="ca3e2-115">Llame a [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar el filtro de AVI en el filtro del escritor de archivos.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="ca3e2-116">Llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la captura de categoría PIN categoría PIN \_ \_ para representar la secuencia de captura.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="ca3e2-117">El generador de gráficos de captura inserta automáticamente el filtro de forma inteligente.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="ca3e2-118">Vuelva a llamar a RenderStream, pero con la categoría de PIN categoría PIN \_ \_ versión preliminar, para representar la secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="ca3e2-119">Omita esta llamada si no desea obtener una vista previa del vídeo.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="ca3e2-120">En el caso de las dos llamadas a RenderStream, el tipo de medio es MEDIATYPE \_ intercalado, es decir, vídeo DV intercalado.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="ca3e2-121">En este código, el generador de gráficos de captura agrega automáticamente todos los filtros necesarios, excepto el filtro de captura MSDV.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca3e2-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca3e2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca3e2-123">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca3e2-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



