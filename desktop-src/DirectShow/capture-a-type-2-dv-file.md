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
# <a name="capture-a-type-2-dv-file"></a>Capturar un archivo de tipo-2 DV

Un archivo AVI de tipo 2 DV tiene dos flujos, uno que contiene vídeo DV y otro que contiene audio. Para capturar un archivo de tipo 2 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.

![captura de tipo 2 con vista previa](images/dv2-cap.png)

Este gráfico es casi el mismo que el gráfico para la captura de tipo 1 (vea [capturar un archivo de tipo 1 DV](capture-a-type-1-dv-file.md)). Sin embargo, el flujo de captura atraviesa el filtro de [divisor de DV](dv-splitter-filter.md) antes de alcanzar el filtro de [AVI](avi-mux-filter.md) . Por tanto, el MUX de AVI recibe dos flujos, una secuencia de audio y una secuencia de vídeo codificada en DV.

Compile este gráfico como se indica a continuación:


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



1.  Cree el divisor de DV y agréguelo al gráfico de filtros.
2.  Llame a [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar el filtro de AVI en el filtro del escritor de archivos.
3.  Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura MSDV al divisor DV. Esta llamada también conecta uno de los pin de salida del divisor DV a AVI Mux.
4.  Vuelva a llamar a RenderStream para conectar el otro PIN del divisor DV a AVI Mux.
5.  Llame a RenderStream una tercera vez para representar la secuencia de vista previa. Omita este paso si no desea obtener una vista previa del vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



