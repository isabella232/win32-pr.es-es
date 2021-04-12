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
# <a name="capture-dv-to-uncompressed-rgb"></a>Capturar DV en RGB sin comprimir

En este ejemplo se muestra cómo capturar DV desde la videocámara y guardarla en un archivo como RGB sin comprimir durante la vista previa. Use el gráfico de filtro que se muestra en el diagrama siguiente.

![capturando RGB sin comprimir en archivo](images/dv-rgb-cap.png)

El filtro de divisor DV divide el audio o vídeo intercalado en secuencias de audio y vídeo independientes el vídeo codificado en DV se dirige al filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) , que genera vídeo RGB sin comprimir. El vídeo RGB se enruta a través del filtro de Smart Tee al filtro de AVI (para la captura) y al representador de vídeo (para la versión preliminar). Mientras tanto, la secuencia de audio del divisor de DV pasa por el filtro tee de anclaje infinito a AVI MUX y el procesador de audio. El administrador de gráficos de filtro mantiene sincronizadas todas estas secuencias, usando las marcas de tiempo de los ejemplos y el reloj de referencia del gráfico.

Este gráfico podría parecer innecesariamente complicado, pero garantiza que la secuencia de vídeo codificada en DV solo se descodifica una vez, lo que minimiza los requisitos de CPU. Además, tenga en cuenta que el vídeo atraviesa el filtro Smart Tee mientras el audio pasa por el filtro tee de anclaje infinito. Smart Tee puede quitar fotogramas de vista previa para mejorar el rendimiento de la captura, lo que es deseable para el vídeo, pero no para el audio, donde las muestras quitadas son muy perceptibles. Además, dado que el audio requiere mucho más ancho de banda que el vídeo, hay relativamente poca probabilidad de que se quite el audio del archivo.

Debe compilar este gráfico una sección a la vez, pero el método RenderStream todavía puede ser de ayuda. Use el código siguiente:


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



Debe crear los filtros de divisor DV, descodificador de vídeo DV, Smart tee y infinita PIN tee y agregar cada uno al gráfico de filtros. (Por motivos de brevedad, estos pasos se omiten en el código anterior). En este ejemplo se usa el método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar los pin de captura y vista previa en el filtro de forma inteligente. la captura siempre es el PIN de salida 0 y la versión preliminar es el PIN de salida 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



