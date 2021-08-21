---
description: Capturar un archivo DV de tipo 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturar un archivo DV de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c944c84ed6cf04ec46de99a209a7b3d2942ae5157bc3ff9d14104da6615d03d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158751"
---
# <a name="capture-a-type-2-dv-file"></a>Capturar un archivo DV de tipo 2

Un archivo AVI DV de tipo 2 tiene dos secuencias, una que contiene vídeo DV y otra que contiene audio. Para capturar un archivo de tipo 2 durante la vista previa, use el gráfico de filtros que se muestra en el diagrama siguiente.

![Captura de tipo 2 con versión preliminar](images/dv2-cap.png)

Este gráfico es casi el mismo que el gráfico para la captura de tipo 1 (vea [Capturar un archivo DV de tipo 1).](capture-a-type-1-dv-file.md) Sin embargo, la secuencia de captura pasa por el filtro [dv splitter](dv-splitter-filter.md) antes de llegar al [filtro Mux de AVI.](avi-mux-filter.md) Por lo tanto, el Mux avi recibe dos secuencias, una secuencia de audio y una secuencia de vídeo codificada en DV.

Compile este gráfico como se muestra a continuación:


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



1.  Cree el divisor DV y agrégrélo al gráfico de filtros.
2.  Llame [**a ICaptureGraphBuilder2::SetOutputFileName para**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) conectar el filtro Mux avi al filtro escritor de archivos.
3.  Llame [**a ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura MSDV al divisor DV. Esta llamada también conecta uno de los pines de salida del divisor DV al Mux avi.
4.  Vuelva a llamar a RenderStream para conectar el otro pin del divisor DV al Mux de AVI.
5.  Llame a RenderStream una tercera vez para representar la secuencia de vista previa. Omita este paso si no desea obtener una vista previa del vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



