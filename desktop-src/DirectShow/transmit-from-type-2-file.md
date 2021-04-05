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
# <a name="transmit-from-type-2-file"></a>Transmisión desde el archivo de tipo 2

Para transmitir un archivo de tipo 2 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.

![tipo-2 transmisión con vista previa](images/dv2-transmit.png)

Un archivo de tipo 2 tiene dos flujos, una secuencia de audio y una secuencia de vídeo codificada en DV. En este gráfico se usa el filtro [DV multiplexor](dv-muxer-filter.md) para combinar las secuencias de audio y vídeo. Envía el flujo intercalado al filtro MSDV, pero vuelve a dividir la secuencia para la vista previa.

Compile este gráfico como se indica a continuación:


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



Este código realiza varias llamadas a **RenderStream**:

Los dos primeros conectan el filtro de origen con el divisor de AVI y el divisor de AVI al DV Mux. En la primera llamada, el generador de gráficos de captura agrega automáticamente el divisor de AVI al gráfico y conecta uno de los clavijas de salida del divisor de AVI con el DV Mux. En la segunda llamada, el generador de gráficos de captura encuentra el segundo PIN de salida del divisor de AVI y lo conecta al DV Mux.

La tercera llamada a **RenderStream** conecta el multiplexor DV al filtro tee del PIN infinito. La siguiente llamada conecta un flujo desde el PIN infinito Tee al filtro de captura MSDV. Esta secuencia se transmite al dispositivo. La última llamada a **RenderStream** crea la sección de vista previa del gráfico.

Si no desea obtener una vista previa durante la transmisión, puede omitir el PIN infinito y simplemente conectar el DV MUX al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



