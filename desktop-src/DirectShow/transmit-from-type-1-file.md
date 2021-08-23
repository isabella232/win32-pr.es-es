---
description: Transmitir desde el archivo de tipo 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmitir desde el archivo de tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ce67627c350c24de1bf1ee96ba7804ac3f164264e167498c597e8136ea138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015542"
---
# <a name="transmit-from-type-1-file"></a>Transmitir desde el archivo de tipo 1

Para transmitir un archivo de tipo 1 al obtener una vista previa del archivo, use el gráfico de filtro que se muestra en el diagrama siguiente.

![transmisión de tipo 1 con versión preliminar](images/dv1-transmit.png)

Los filtros de este gráfico incluyen:

-   El [divisor AVI](avi-splitter-filter.md) analiza el archivo AVI. Para un archivo DV de tipo 1, el pin de salida proporciona ejemplos de DV intercalados.
-   El [filtro Infinite Pin Tee](infinite-pin-tee-filter.md) divide la DV intercalada en una secuencia de transmisión y una secuencia de vista previa. Ambas secuencias contienen los mismos datos intercalados. (Este gráfico usa la tea de pin infinito en lugar de smart [tee](smart-tee-filter.md), porque no hay peligro de quitar fotogramas al leer desde un archivo, como ocurre con la captura en vivo).
-   El [divisor DV](dv-splitter-filter.md) divide la secuencia intercalada en una secuencia de vídeo DV, que se descodifica mediante el descodificador de vídeo [DV](dv-video-decoder-filter.md)y una secuencia de audio. Ambas secuencias se representados para la versión preliminar.

Compile este gráfico como se muestra a continuación:


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



1.  Llame [**a IGraphBuilder::AddSourceFilter para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) agregar el filtro de origen al gráfico de filtro.
2.  Cree el divisor AVI y la te de pin infinito y agrégrélos al gráfico.
3.  Llame [**a ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de origen al divisor AVI. Especificar MEDIATYPE intercalado para asegurarse de que se produce un error en el método si el archivo de origen \_ no es un archivo DV de tipo 1. En ese caso, puede volver atrás e intentar crear un gráfico de transmisión de tipo 2 en su lugar.
4.  Vuelva **a llamar a RenderStream** para enrutar la secuencia intercalada desde el divisor AVI a la te de pin infinito
5.  Llame a RenderStream una tercera vez para enrutar una secuencia desde la tea de pin infinito al filtro MSDV, para transmitir al dispositivo.
6.  Llame **a RenderStream** una última vez para compilar la sección de vista previa del gráfico.

Si no desea obtener una vista previa, simplemente conecte el origen de archivo al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



