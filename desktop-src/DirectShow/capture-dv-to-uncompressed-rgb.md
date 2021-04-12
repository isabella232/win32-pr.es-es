---
description: Capturar DV en RGB sin comprimir
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturar DV en RGB sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152044"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="18823-103">Capturar DV en RGB sin comprimir</span><span class="sxs-lookup"><span data-stu-id="18823-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="18823-104">En este ejemplo se muestra cómo capturar DV desde la videocámara y guardarla en un archivo como RGB sin comprimir durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="18823-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="18823-105">Use el gráfico de filtro que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="18823-105">Use the filter graph shown in the following diagram.</span></span>

![capturando RGB sin comprimir en archivo](images/dv-rgb-cap.png)

<span data-ttu-id="18823-107">El filtro de divisor DV divide el audio o vídeo intercalado en secuencias de audio y vídeo independientes el vídeo codificado en DV se dirige al filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) , que genera vídeo RGB sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="18823-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="18823-108">El vídeo RGB se enruta a través del filtro de Smart Tee al filtro de AVI (para la captura) y al representador de vídeo (para la versión preliminar).</span><span class="sxs-lookup"><span data-stu-id="18823-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="18823-109">Mientras tanto, la secuencia de audio del divisor de DV pasa por el filtro tee de anclaje infinito a AVI MUX y el procesador de audio.</span><span class="sxs-lookup"><span data-stu-id="18823-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="18823-110">El administrador de gráficos de filtro mantiene sincronizadas todas estas secuencias, usando las marcas de tiempo de los ejemplos y el reloj de referencia del gráfico.</span><span class="sxs-lookup"><span data-stu-id="18823-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="18823-111">Este gráfico podría parecer innecesariamente complicado, pero garantiza que la secuencia de vídeo codificada en DV solo se descodifica una vez, lo que minimiza los requisitos de CPU.</span><span class="sxs-lookup"><span data-stu-id="18823-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="18823-112">Además, tenga en cuenta que el vídeo atraviesa el filtro Smart Tee mientras el audio pasa por el filtro tee de anclaje infinito.</span><span class="sxs-lookup"><span data-stu-id="18823-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="18823-113">Smart Tee puede quitar fotogramas de vista previa para mejorar el rendimiento de la captura, lo que es deseable para el vídeo, pero no para el audio, donde las muestras quitadas son muy perceptibles.</span><span class="sxs-lookup"><span data-stu-id="18823-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="18823-114">Además, dado que el audio requiere mucho más ancho de banda que el vídeo, hay relativamente poca probabilidad de que se quite el audio del archivo.</span><span class="sxs-lookup"><span data-stu-id="18823-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="18823-115">Debe compilar este gráfico una sección a la vez, pero el método RenderStream todavía puede ser de ayuda.</span><span class="sxs-lookup"><span data-stu-id="18823-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="18823-116">Use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="18823-116">Use the following code:</span></span>


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



<span data-ttu-id="18823-117">Debe crear los filtros de divisor DV, descodificador de vídeo DV, Smart tee y infinita PIN tee y agregar cada uno al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="18823-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="18823-118">(Por motivos de brevedad, estos pasos se omiten en el código anterior). En este ejemplo se usa el método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar los pin de captura y vista previa en el filtro de forma inteligente. la captura siempre es el PIN de salida 0 y la versión preliminar es el PIN de salida 1.</span><span class="sxs-lookup"><span data-stu-id="18823-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18823-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18823-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18823-120">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="18823-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



