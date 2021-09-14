---
description: Creación de gráficos con capture Graph Builder
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Creación de gráficos con capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161672"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Creación de gráficos con capture Graph Builder

A pesar de su nombre, capture Graph Builder es útil para crear muchos tipos de gráficos de filtro personalizados, no solo para capturar gráficos. En este artículo se proporciona una breve introducción sobre cómo usar este objeto.

Capture Graph Builder expone la [**interfaz ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Para empezar, [**llame a CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear capture Graph Builder y filter Graph Manager. A continuación, inicialice capture Graph Builder mediante una llamada a [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero al Administrador de Graph filtros, como se muestra a continuación:


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



## <a name="connecting-filters"></a>Conectar filtros

El [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conecta dos o tres filtros en una cadena. Por lo general, el método funciona mejor cuando cada filtro no tiene más de un pin de entrada o un pin de salida del mismo tipo. Esta discusión comienza omitiendo los dos primeros parámetros de **RenderStream** y centrándose en los tres últimos parámetros. El tercer parámetro es un [**puntero IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que puede especificar un filtro (como un puntero de interfaz [**IBaseFilter)**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) o un pin de salida (como puntero de interfaz [**IPin).**](/windows/desktop/api/Strmif/nn-strmif-ipin) Los parámetros cuarto y quinto especifican **punteros IBaseFilter.** El **método RenderStream** conecta los tres filtros de una cadena. Por ejemplo, supongamos que *A,* *B* y *C* son filtros. Supongamos por ahora que cada filtro tiene exactamente un pin de entrada y un pin de salida. La siguiente llamada conecta A a B y, a continuación, B a C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Todas las conexiones son "inteligentes", lo que significa que se agregan filtros adicionales al gráfico según sea necesario. Para obtener más información, [consulte Intelligent Conectar](intelligent-connect.md). Para conectar solo dos filtros, establezca el valor medio en **NULL.** Por ejemplo, esta llamada conecta A a C:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Puede crear cadenas más largas llamando al método dos veces:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Si el último parámetro es **NULL,** el método busca automáticamente un representador predeterminado. Usa el [representador de vídeo para](video-renderer-filter.md) vídeo y el [representador de Direct Sound para](directsound-renderer-filter.md) audio. Así:

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

es equivalente a

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

donde *R* es el representador adecuado. Para conectar el filtro Representador de mezcla de vídeo en lugar del representador de vídeo, debe especificarlo explícitamente.

Si especifica un filtro en el tercer parámetro, en lugar de un pin, es posible que tenga que indicar qué pin de salida se debe usar para la conexión. Ese es el propósito de los dos primeros parámetros del método. El primer parámetro solo se aplica a los filtros de captura. Especifica un GUID que indica una categoría de pin. Para obtener una lista completa de categorías, vea [Anclar conjunto de propiedades.](pin-property-set.md) Dos de las categorías son válidas para todos los filtros de captura:

-   **CAPTURA DE \_ CATEGORÍA DE \_ PIN**
-   **VISTA PREVIA \_ DE CATEGORÍA DE \_ PIN**

Si un filtro de captura no proporciona pasadores independientes para la captura y la vista previa, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta un filtro [Smart Tee,](smart-tee-filter.md) que divide la secuencia en una secuencia de captura y una secuencia de vista previa. Desde el punto de vista de la aplicación, simplemente puede tratar todos los filtros de captura como que tienen pasadores independientes e ignorar la topología subyacente del gráfico.

Para la captura de archivos, conecte el pin de captura a un filtro mux. Para obtener una vista previa en vivo, conecte el pin de vista previa a un representador. Si cambia las dos categorías, el gráfico podría quitar un número excesivo de fotogramas durante la captura de archivos. pero si el gráfico está conectado correctamente, quita los fotogramas de vista previa según sea necesario para mantener el rendimiento en la secuencia de captura.

En el ejemplo siguiente se muestra cómo conectar ambas secuencias:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Algunos filtros de captura también admiten subtítulos, indicados por **PIN \_ CATEGORY \_ VBI**. Para capturar los subtítulos en un archivo, represente esta categoría en el filtro mux. Para ver los subtítulos en la ventana de vista previa, conéctese al representador:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



El segundo parámetro de [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica el tipo de medio y suele ser uno de los siguientes:

-   MEDIATYPE \_ Audio
-   VÍDEO \_ MEDIATYPE
-   MEDIATYPE \_ intercalado (DV)

Puede usar este parámetro siempre que los pines de salida del filtro admitan la enumeración de tipos de medios preferidos. En el caso de los orígenes de archivos, capture Graph Builder agrega automáticamente un filtro de analizador si es necesario y, a continuación, consulta los tipos de medios en el analizador. (Para obtener un ejemplo, vea [Volver acomprimir un archivo AVI).](recompressing-an-avi-file.md) Además, si el último filtro de la cadena tiene varios pines de entrada, el método intenta enumerar sus tipos de medios. Sin embargo, no todos los filtros admiten esta funcionalidad.

## <a name="finding-interfaces-on-filters-and-pins"></a>Buscar interfaces en filtros y pines

Después de crear un gráfico, normalmente deberá buscar varias interfaces expuestas por filtros y anclados en el gráfico. Por ejemplo, un filtro de captura podría exponer la interfaz [**IAMDroppedFrames,**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) mientras que los pines de salida del filtro podrían exponer la [**interfaz IAMStreamConfig.**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)

La manera más sencilla de buscar una interfaz es usar el [**método ICaptureGraphBuilder2::FindInterface.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) Este método recorre el gráfico (filtros y anclados) hasta que encuentra la interfaz deseada. Puede especificar el punto inicial de la búsqueda y limitar la búsqueda a los filtros ascendentes o descendentes desde el punto inicial.

En el ejemplo siguiente se busca la [**interfaz IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en un pin de vista previa de vídeo:


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
> El tema [Buscar una interfaz en un](find-an-interface-on-a-filter-or-pin.md) filtro o un pin muestra un enfoque alternativo que usa la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) en lugar de [**ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) El enfoque que se debe usar depende de la aplicación. Si la aplicación ya usa **ICaptureGraphBuilder2** para compilar el gráfico, [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) es un buen enfoque. De lo contrario, considere la posibilidad de usar **los métodos IGraphBuilder.**

 

## <a name="finding-pins"></a>Búsqueda de pins

Normalmente, es posible que deba buscar un pin individual en un filtro, aunque en la mayoría de los casos los métodos [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) y [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) le ahorrarán el problema. Si necesita encontrar un pin determinado en un filtro, el método auxiliar [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) es útil. Especifique la categoría, el tipo de medio (vídeo o audio), la dirección y si el pin debe estar desconectado.

Por ejemplo, el código siguiente busca una clavija de vista previa de vídeo no conectada en un filtro de captura:


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

 

 
