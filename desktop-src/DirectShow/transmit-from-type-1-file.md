---
description: Transmisión del archivo de tipo 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmisión del archivo de tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082800"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="d0e70-103">Transmisión del archivo de tipo 1</span><span class="sxs-lookup"><span data-stu-id="d0e70-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="d0e70-104">Para transmitir un archivo de tipo 1 mientras se muestra la vista previa del archivo, use el gráfico de filtro que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0e70-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![tipo-1 transmisión con vista previa](images/dv1-transmit.png)

<span data-ttu-id="d0e70-106">Los filtros de este grafo incluyen:</span><span class="sxs-lookup"><span data-stu-id="d0e70-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="d0e70-107">El [divisor de AVI](avi-splitter-filter.md) analiza el archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="d0e70-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="d0e70-108">En el caso de un archivo DV de tipo 1, el PIN de salida proporciona muestras de DV intercaladas.</span><span class="sxs-lookup"><span data-stu-id="d0e70-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="d0e70-109">El filtro [tee de anclaje infinito](infinite-pin-tee-filter.md) divide el DV intercalado en una secuencia de transmisión y en una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="d0e70-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="d0e70-110">Ambas secuencias contienen los mismos datos intercalados.</span><span class="sxs-lookup"><span data-stu-id="d0e70-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="d0e70-111">(Este gráfico usa el PIN infinito Tee en lugar de [Smart Tee](smart-tee-filter.md), ya que no hay ningún riesgo de quitar fotogramas al leer desde un archivo, como si se tratase de una captura en directo).</span><span class="sxs-lookup"><span data-stu-id="d0e70-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="d0e70-112">El [divisor DV](dv-splitter-filter.md) divide la secuencia intercalada en una secuencia de vídeo DV, descodificada por el [descodificador de vídeo DV](dv-video-decoder-filter.md)y una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="d0e70-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="d0e70-113">Ambos flujos se rendererd para la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="d0e70-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="d0e70-114">Compile este gráfico como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d0e70-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="d0e70-115">Llame a [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar el filtro de origen al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d0e70-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="d0e70-116">Cree el divisor de AVI y el PIN infinito tee y agréguelos al gráfico.</span><span class="sxs-lookup"><span data-stu-id="d0e70-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="d0e70-117">Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de origen al divisor de AVI.</span><span class="sxs-lookup"><span data-stu-id="d0e70-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="d0e70-118">Especificar MEDIATYPE \_ intercalado para asegurarse de que se produce un error en el método si el archivo de origen no es un archivo DV de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="d0e70-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="d0e70-119">En ese caso, puede hacer una copia de seguridad e intentar compilar un gráfico de transmisión de tipo 2 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d0e70-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="d0e70-120">Vuelva a llamar a **RenderStream** para enrutar el flujo intercalado desde el divisor de AVI hasta el anclaje infinito.</span><span class="sxs-lookup"><span data-stu-id="d0e70-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="d0e70-121">Llame a RenderStream una tercera vez para enrutar una secuencia desde el PIN infinito y Tee al filtro MSDV para transmitirla al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0e70-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="d0e70-122">Llame a **RenderStream** una vez por última vez para compilar la sección de vista previa del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d0e70-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="d0e70-123">Si no desea obtener una vista previa, simplemente conecte el origen del archivo al filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="d0e70-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="d0e70-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0e70-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0e70-125">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d0e70-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



