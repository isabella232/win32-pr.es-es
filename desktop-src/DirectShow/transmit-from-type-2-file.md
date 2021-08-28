---
description: Transmisión desde un archivo de tipo 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmisión desde un archivo de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315725"
---
# <a name="transmit-from-type-2-file"></a>Transmisión desde un archivo de tipo 2

Para transmitir un archivo de tipo 2 durante la vista previa, use el gráfico de filtros que se muestra en el diagrama siguiente.

![Transmisión de tipo 2 con versión preliminar](images/dv2-transmit.png)

Un archivo de tipo 2 tiene dos secuencias, una secuencia de audio y una secuencia de vídeo codificada en DV. Este gráfico usa el [filtro DV Muxer](dv-muxer-filter.md) para combinar las secuencias de audio y vídeo. Envía la secuencia intercalada al filtro MSDV, pero divide la secuencia de nuevo para la versión preliminar.

Compile este gráfico como se muestra a continuación:


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



Este código realiza varias llamadas a **RenderStream:**

Los dos primeros conectan el filtro de origen al divisor AVI y el divisor AVI al Mux dv. En la primera llamada, Capture Graph Builder agrega automáticamente el divisor AVI al gráfico y conecta una de las clavijas de salida del divisor AVI al Mux de DV. En la segunda llamada, Capture Graph Builder busca el segundo pin de salida del divisor AVI y lo conecta al Mux dv.

La tercera llamada a **RenderStream** conecta el Muxer dv al filtro infinite pin tee. La siguiente llamada conecta una secuencia desde la tee de pin infinito al filtro de captura de MSDV. Esta secuencia se transmite al dispositivo. La última llamada a **RenderStream** compila la sección de vista previa del gráfico.

Si no desea obtener una vista previa durante la transmisión, puede omitir la tee de pin infinito y simplemente conectar el Mux dv al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



