---
description: Capturar un archivo DV de tipo 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturar un archivo DV de tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb6621daab2721970cfc8651ff343ebcb4c4988aa88c1815466011de0f560db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652535"
---
# <a name="capture-a-type-1-dv-file"></a>Capturar un archivo DV de tipo 1

Un archivo AVI DV de tipo 1 contiene una única secuencia intercalada. Para capturar un archivo de tipo 1 durante la vista previa, use el gráfico de filtros que se muestra en el diagrama siguiente.

![Captura de tipo 1 con versión preliminar](images/dv1-cap.png)

Los filtros de este gráfico incluyen:

-   El [filtro Smart Tee](smart-tee-filter.md) divide la DV intercalada en una secuencia de captura y una secuencia de vista previa. Ambas secuencias contienen los mismos datos intercalados.
-   Avi [Mux y](avi-mux-filter.md) [File Writer](file-writer-filter.md) escriben la secuencia intercalada en el disco.
-   El [divisor DV](dv-splitter-filter.md) divide la secuencia intercalada en una secuencia de vídeo DV y una secuencia de audio. Ambas secuencias se representados para la versión preliminar.
-   El [descodificador de vídeo DV](dv-video-decoder-filter.md) descodifica la secuencia de vídeo DV para la vista previa.

Compile este gráfico como se muestra a continuación:


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



1.  Llame [**a ICaptureGraphBuilder2::SetOutputFileName para**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) conectar el filtro avi Mux al filtro File Writer.
2.  Llame [**a ICaptureGraphBuilder2::RenderStream con**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) la categoría PIN CATEGORY CAPTURE para representar la secuencia de \_ \_ captura. Capture Graph Builder inserta automáticamente el filtro Smart Tee.
3.  Vuelva a llamar a RenderStream, pero con la categoría PIN \_ CATEGORY PREVIEW para representar la secuencia de vista \_ previa. Omita esta llamada si no desea obtener una vista previa del vídeo.

Para ambas llamadas a RenderStream, el tipo de medio es MEDIATYPE Intercalado, lo que significa \_ vídeo DV intercalado. En este código, capture Graph Builder agrega automáticamente todos los filtros necesarios, excepto el filtro de captura MSDV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



