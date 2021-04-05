---
description: Transmisión desde el archivo de tipo 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmisión desde el archivo de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002154"
---
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="748de-103">Transmisión desde el archivo de tipo 2</span><span class="sxs-lookup"><span data-stu-id="748de-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="748de-104">Para transmitir un archivo de tipo 2 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="748de-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![tipo-2 transmisión con vista previa](images/dv2-transmit.png)

<span data-ttu-id="748de-106">Un archivo de tipo 2 tiene dos flujos, una secuencia de audio y una secuencia de vídeo codificada en DV.</span><span class="sxs-lookup"><span data-stu-id="748de-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="748de-107">En este gráfico se usa el filtro [DV multiplexor](dv-muxer-filter.md) para combinar las secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="748de-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="748de-108">Envía el flujo intercalado al filtro MSDV, pero vuelve a dividir la secuencia para la vista previa.</span><span class="sxs-lookup"><span data-stu-id="748de-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="748de-109">Compile este gráfico como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="748de-109">Build this graph as follows:</span></span>


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



<span data-ttu-id="748de-110">Este código realiza varias llamadas a **RenderStream**:</span><span class="sxs-lookup"><span data-stu-id="748de-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="748de-111">Los dos primeros conectan el filtro de origen con el divisor de AVI y el divisor de AVI al DV Mux.</span><span class="sxs-lookup"><span data-stu-id="748de-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="748de-112">En la primera llamada, el generador de gráficos de captura agrega automáticamente el divisor de AVI al gráfico y conecta uno de los clavijas de salida del divisor de AVI con el DV Mux.</span><span class="sxs-lookup"><span data-stu-id="748de-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="748de-113">En la segunda llamada, el generador de gráficos de captura encuentra el segundo PIN de salida del divisor de AVI y lo conecta al DV Mux.</span><span class="sxs-lookup"><span data-stu-id="748de-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="748de-114">La tercera llamada a **RenderStream** conecta el multiplexor DV al filtro tee del PIN infinito.</span><span class="sxs-lookup"><span data-stu-id="748de-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="748de-115">La siguiente llamada conecta un flujo desde el PIN infinito Tee al filtro de captura MSDV.</span><span class="sxs-lookup"><span data-stu-id="748de-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="748de-116">Esta secuencia se transmite al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="748de-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="748de-117">La última llamada a **RenderStream** crea la sección de vista previa del gráfico.</span><span class="sxs-lookup"><span data-stu-id="748de-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="748de-118">Si no desea obtener una vista previa durante la transmisión, puede omitir el PIN infinito y simplemente conectar el DV MUX al filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="748de-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="748de-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="748de-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748de-120">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="748de-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



