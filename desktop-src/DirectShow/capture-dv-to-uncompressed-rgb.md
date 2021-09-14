---
description: Capturar DV en RGB sin comprimir
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturar DV en RGB sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160228"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Capturar DV en RGB sin comprimir

En este ejemplo se muestra cómo capturar DV de la cámara de vídeo y guardarlo en un archivo como RGB sin comprimir durante la vista previa. Use el gráfico de filtro que se muestra en el diagrama siguiente.

![captura de rgb sin comprimir en el archivo](images/dv-rgb-cap.png)

El filtro divisor DV divide el audio o vídeo intercalado en secuencias de audio y vídeo independientes. El vídeo codificado en DV va al filtro Descodificador de vídeo [DV,](dv-video-decoder-filter.md) que genera vídeo RGB sin comprimir. El vídeo RGB se enruta a través del filtro Smart Tee al filtro Mux avi (para la captura) y al representador de vídeo (para la versión preliminar). Mientras tanto, la secuencia de audio del divisor DV pasa a través del filtro Infinite Pin Tee (Tee de pin infinito) al Mux avi y al representador de audio. Filter Graph Manager mantiene todas estas secuencias sincronizadas, usando las marcas de tiempo en los ejemplos y el reloj de referencia del gráfico.

Este gráfico puede parecer innecesariamente complicado, pero garantiza que la secuencia de vídeo codificada en DV solo se descodifica una vez, lo que minimiza los requisitos de CPU. Además, tenga en cuenta que el vídeo pasa por el filtro Smart Tee mientras el audio pasa por el filtro Infinite Pin Tee. Smart Tee puede quitar fotogramas de vista previa para mejorar el rendimiento de la captura, lo que es deseable para el vídeo, pero no para el audio, donde las muestras descartadas son muy evidentes. Además, dado que el audio requiere un ancho de banda mucho menor que el vídeo, hay relativamente pocas posibilidades de colocar audio en el archivo.

Debe compilar este gráfico una sección a la vez, pero el método RenderStream puede seguir siendo de ayuda. Use el código siguiente:


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



Debe crear los filtros DV Splitter, DV Video Decoder, Smart Tee y Infinite Pin Tee y agregar cada uno al gráfico de filtros. (Por brevedad, estos pasos se omiten del código anterior). En este ejemplo se [**usa el método ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar los pines de captura y vista previa en el filtro Smart Tee; capture siempre es el pin de salida 0 y la vista previa es el pin de salida 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



