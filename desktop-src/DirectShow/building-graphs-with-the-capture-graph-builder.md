---
description: Generar gráficos con el generador de gráficos de captura
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Generar gráficos con el generador de gráficos de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906822"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Generar gráficos con el generador de gráficos de captura

A pesar de su nombre, el generador de gráficos de captura es útil para crear muchos tipos de gráficos de filtros personalizados, no solo para capturar gráficos. En este artículo se proporciona una breve descripción de cómo utilizar este objeto.

El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Empiece por llamar a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el generador de gráficos de captura y el administrador de gráficos de filtro. A continuación, inicialice el generador de gráficos de captura mediante una llamada a [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero al administrador de gráficos de filtro, como se indica a continuación:


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Conexión de filtros

El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conecta dos o tres filtros juntos en una cadena. Por lo general, el método funciona mejor cuando cada filtro no tiene más de un PIN de entrada o de salida del mismo tipo. Este debate comienza omitiendo los dos primeros parámetros de **RenderStream** y centrándose en los tres últimos parámetros. El tercer parámetro es un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que puede especificar un filtro (como un puntero de interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) o un PIN de salida (como un puntero de interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ). Los parámetros cuarto y quinto especifican punteros **IBaseFilter** . El método **RenderStream** conecta los tres filtros de una cadena. Por ejemplo, suponga que *A*, *B* y *C* son filtros. Supongamos por ahora que cada filtro tiene exactamente un PIN de entrada y uno de salida. La siguiente llamada conecta a a B y, a continuación, B a C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Todas las conexiones son "inteligentes", lo que significa que los filtros adicionales se agregan al gráfico según sea necesario. Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md). Para conectar solo dos filtros, establezca el valor intermedio en **null**. Por ejemplo, esta llamada conecta a a C:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Puede crear cadenas más largas llamando al método dos veces:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Si el último parámetro es **null**, el método busca automáticamente un representador predeterminado. Usa el [representador de vídeo](video-renderer-filter.md) para vídeo y el [representador de DirectSound](directsound-renderer-filter.md) para audio. Modo

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

es equivalente a

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

donde *R* es el representador adecuado. Sin embargo, para conectar el filtro de representador de mezcla de vídeo en lugar del representador de vídeo, debe especificarlo explícitamente.

Si especifica un filtro en el tercer parámetro, en lugar de un PIN, es posible que deba indicar qué PIN de salida se debe usar para la conexión. Este es el propósito de los dos primeros parámetros del método. El primer parámetro solo se aplica a los filtros de captura. Especifica un GUID que indica una categoría de PIN. Para obtener una lista completa de las categorías, vea [conjunto de propiedades del PIN](pin-property-set.md). Dos de las categorías son válidas para todos los filtros de captura:

-   **\_captura de categoría de PIN \_**
-   **\_vista previa de categoría de PIN \_**

Si un filtro de captura no proporciona clavijas independientes para la captura y la vista previa, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta un filtro de forma [inteligente](smart-tee-filter.md) , que divide la secuencia en una secuencia de captura y una secuencia de vista previa. Desde el punto de vista de la aplicación, puede tratar simplemente todos los filtros de captura como si tuvieran PIN independientes y omitir la topología subyacente del gráfico.

Para la captura de archivos, conecte el PIN de captura a un filtro Mux. Para la vista previa dinámica, conecte el PIN de vista previa a un representador. Si cambia las dos categorías, el gráfico podría quitar un número excesivo de fotogramas durante la captura de archivos. pero si el gráfico está conectado correctamente, quita los fotogramas de vista previa según sea necesario para mantener el rendimiento en la secuencia de captura.

En el ejemplo siguiente se muestra cómo conectar ambos flujos:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Algunos filtros de captura también admiten subtítulos (CC), que se indican mediante la **categoría de PIN \_ \_ VBI**. Para capturar los subtítulos cerrados en un archivo, represente esta categoría al filtro Mux. Para ver los subtítulos cerrados en la ventana de vista previa, conéctese al representador:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



El segundo parámetro de [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica el tipo de medio y suele ser uno de los siguientes:

-   Audio de MEDIATYPE \_
-   Vídeo de MEDIATYPE \_
-   MEDIATYPE \_ intercalado (DV)

Puede usar este parámetro siempre que los pin de salida del filtro admitan la enumeración de los tipos de medios preferidos. En el caso de los orígenes de archivos, el generador de gráficos de captura agrega automáticamente un filtro de analizador si es necesario y, a continuación, consulta los tipos de medios en el analizador. (Para obtener un ejemplo, vea [recomprimir un archivo AVI](recompressing-an-avi-file.md)). Además, si el último filtro de la cadena tiene varios PIN de entrada, el método intenta enumerar sus tipos de medios. Sin embargo, no todos los filtros admiten esta funcionalidad.

## <a name="finding-interfaces-on-filters-and-pins"></a>Buscar interfaces en filtros y PIN

Después de compilar un gráfico, normalmente necesitará encontrar varias interfaces expuestas por filtros y clavijas en el gráfico. Por ejemplo, un filtro de captura podría exponer la interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , mientras que los pin de salida del filtro podrían exponer la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .

La manera más sencilla de encontrar una interfaz es usar el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) . Este método recorre el gráfico (filtros y clavijas) hasta que encuentra la interfaz deseada. Puede especificar el punto de partida de la búsqueda y puede limitar la búsqueda a los filtros que se encadenan hacia arriba o hacia abajo desde el punto de partida.

En el ejemplo siguiente se busca la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en un PIN de vista previa de vídeo:


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> En el tema [buscar una interfaz en un filtro o un PIN](find-an-interface-on-a-filter-or-pin.md) se muestra un enfoque alternativo que usa la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) en lugar de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2). El enfoque que se debe usar depende de la aplicación. Si la aplicación ya usa **ICaptureGraphBuilder2** para compilar el gráfico, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) es un buen enfoque. En caso contrario, considere la posibilidad de usar los métodos **IGraphBuilder** .

 

## <a name="finding-pins"></a>Buscar PIN

Con menos frecuencia, es posible que necesite buscar un PIN individual en un filtro, aunque en la mayoría de los casos los métodos [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) y [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) le ahorrarán el problema. Si necesita buscar un PIN determinado en un filtro, el método auxiliar [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) es útil. Especifique la categoría, el tipo de medio (vídeo o audio), la dirección y si el PIN debe estar desconectado.

Por ejemplo, el código siguiente busca un PIN de vista previa de vídeo no conectado en un filtro de captura:


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
