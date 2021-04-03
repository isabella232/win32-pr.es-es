---
description: Capturar un archivo de tipo-2 DV
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturar un archivo de tipo-2 DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906383"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="aa0ae-103">Capturar un archivo de tipo-2 DV</span><span class="sxs-lookup"><span data-stu-id="aa0ae-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="aa0ae-104">Un archivo AVI de tipo 2 DV tiene dos flujos, uno que contiene vídeo DV y otro que contiene audio.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="aa0ae-105">Para capturar un archivo de tipo 2 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![captura de tipo 2 con vista previa](images/dv2-cap.png)

<span data-ttu-id="aa0ae-107">Este gráfico es casi el mismo que el gráfico para la captura de tipo 1 (vea [capturar un archivo de tipo 1 DV](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="aa0ae-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="aa0ae-108">Sin embargo, el flujo de captura atraviesa el filtro de [divisor de DV](dv-splitter-filter.md) antes de alcanzar el filtro de [AVI](avi-mux-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0ae-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="aa0ae-109">Por tanto, el MUX de AVI recibe dos flujos, una secuencia de audio y una secuencia de vídeo codificada en DV.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="aa0ae-110">Compile este gráfico como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="aa0ae-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="aa0ae-111">Cree el divisor de DV y agréguelo al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="aa0ae-112">Llame a [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar el filtro de AVI en el filtro del escritor de archivos.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="aa0ae-113">Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura MSDV al divisor DV.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="aa0ae-114">Esta llamada también conecta uno de los pin de salida del divisor DV a AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="aa0ae-115">Vuelva a llamar a RenderStream para conectar el otro PIN del divisor DV a AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="aa0ae-116">Llame a RenderStream una tercera vez para representar la secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="aa0ae-117">Omita este paso si no desea obtener una vista previa del vídeo.</span><span class="sxs-lookup"><span data-stu-id="aa0ae-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa0ae-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa0ae-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa0ae-119">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa0ae-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



