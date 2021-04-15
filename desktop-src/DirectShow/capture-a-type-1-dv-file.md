---
description: Capturar un archivo de tipo 1 DV
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturar un archivo de tipo 1 DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556445"
---
# <a name="capture-a-type-1-dv-file"></a>Capturar un archivo de tipo 1 DV

Un archivo AVI de tipo 1 digital contiene una única secuencia intercalada. Para capturar un archivo de tipo 1 durante la vista previa, use el gráfico de filtro que se muestra en el diagrama siguiente.

![captura de tipo 1 con vista previa](images/dv1-cap.png)

Los filtros de este grafo incluyen:

-   Este [filtro divide el DV](smart-tee-filter.md) intercalado en una secuencia de captura y en una secuencia de vista previa. Ambas secuencias contienen los mismos datos intercalados.
-   [AVI MUX](avi-mux-filter.md) y el [escritor de archivos](file-writer-filter.md) escriben el flujo intercalado en el disco.
-   El [divisor DV](dv-splitter-filter.md) divide el flujo intercalado en una secuencia de vídeo DV y en una secuencia de audio. Ambos flujos se rendererd para la versión preliminar.
-   El [descodificador de vídeo DV](dv-video-decoder-filter.md) descodifica el flujo de vídeo DV para la vista previa.

Compile este gráfico como se indica a continuación:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Llame a [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar el filtro de AVI en el filtro del escritor de archivos.
2.  Llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la captura de categoría PIN categoría PIN \_ \_ para representar la secuencia de captura. El generador de gráficos de captura inserta automáticamente el filtro de forma inteligente.
3.  Vuelva a llamar a RenderStream, pero con la categoría de PIN categoría PIN \_ \_ versión preliminar, para representar la secuencia de vista previa. Omita esta llamada si no desea obtener una vista previa del vídeo.

En el caso de las dos llamadas a RenderStream, el tipo de medio es MEDIATYPE \_ intercalado, es decir, vídeo DV intercalado. En este código, el generador de gráficos de captura agrega automáticamente todos los filtros necesarios, excepto el filtro de captura MSDV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



