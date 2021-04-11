---
description: Transmisión del archivo de tipo 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmisión del archivo de tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082800"
---
# <a name="transmit-from-type-1-file"></a>Transmisión del archivo de tipo 1

Para transmitir un archivo de tipo 1 mientras se muestra la vista previa del archivo, use el gráfico de filtro que se muestra en el diagrama siguiente.

![tipo-1 transmisión con vista previa](images/dv1-transmit.png)

Los filtros de este grafo incluyen:

-   El [divisor de AVI](avi-splitter-filter.md) analiza el archivo AVI. En el caso de un archivo DV de tipo 1, el PIN de salida proporciona muestras de DV intercaladas.
-   El filtro [tee de anclaje infinito](infinite-pin-tee-filter.md) divide el DV intercalado en una secuencia de transmisión y en una secuencia de vista previa. Ambas secuencias contienen los mismos datos intercalados. (Este gráfico usa el PIN infinito Tee en lugar de [Smart Tee](smart-tee-filter.md), ya que no hay ningún riesgo de quitar fotogramas al leer desde un archivo, como si se tratase de una captura en directo).
-   El [divisor DV](dv-splitter-filter.md) divide la secuencia intercalada en una secuencia de vídeo DV, descodificada por el [descodificador de vídeo DV](dv-video-decoder-filter.md)y una secuencia de audio. Ambos flujos se rendererd para la versión preliminar.

Compile este gráfico como se indica a continuación:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  Llame a [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar el filtro de origen al gráfico de filtro.
2.  Cree el divisor de AVI y el PIN infinito tee y agréguelos al gráfico.
3.  Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de origen al divisor de AVI. Especificar MEDIATYPE \_ intercalado para asegurarse de que se produce un error en el método si el archivo de origen no es un archivo DV de tipo 1. En ese caso, puede hacer una copia de seguridad e intentar compilar un gráfico de transmisión de tipo 2 en su lugar.
4.  Vuelva a llamar a **RenderStream** para enrutar el flujo intercalado desde el divisor de AVI hasta el anclaje infinito.
5.  Llame a RenderStream una tercera vez para enrutar una secuencia desde el PIN infinito y Tee al filtro MSDV para transmitirla al dispositivo.
6.  Llame a **RenderStream** una vez por última vez para compilar la sección de vista previa del gráfico.

Si no desea obtener una vista previa, simplemente conecte el origen del archivo al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



