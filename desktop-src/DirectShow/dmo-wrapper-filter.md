---
description: Filtro de contenedor de DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Filtro de contenedor de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b01ee006203e2e1fd328bacc13c01de4a3b25f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495580"
---
# <a name="dmo-wrapper-filter"></a>Filtro de contenedor de DMO

El filtro de contenedor de DMO permite a una aplicación de DirectShow usar un [objeto multimedia de DirectX](directx-media-objects.md) (DMO) dentro de un gráfico de filtros. El filtro contiene DMO y controla todos los detalles del uso de DMO, como pasar datos hacia y desde DMO. Además, el filtro agrega DMO, por lo que la aplicación puede consultar el filtro para las interfaces COM que expone el DMO.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipos de medios de anclaje de entrada                    | Ver comentarios                                                                                                                                                                                                                                        |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de anclaje de salida                   | Ver comentarios                                                                                                                                                                                                                                        |
| Interfaces de clavija de salida                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                   |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Fundament](merit.md)                       | Ver comentarios                                                                                                                                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | Ver comentarios                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

### <a name="limitations"></a>Limitaciones

El contenedor de DMO tiene las siguientes limitaciones:

-   No admite DMOs con cero entradas, entradas múltiples o salidas cero. (Admite DMOs con una entrada y varias salidas).
-   No admite transportes personalizados. Todo el transporte de datos se realiza a través de la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   No usa la interfaz **IMediaObjectInPlace** ; todo el procesamiento se realiza mediante métodos [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Chinchetas

Para cada flujo de entrada de DMO, el filtro crea un PIN de entrada correspondiente. Para cada flujo de salida, se crea un PIN de salida correspondiente. Los tipos de medios que admite cada pin dependen de DMO

### <a name="encoder-interfaces"></a>Interfaces del codificador

Si DMO es un codificador de vídeo o un codificador de audio, el PIN de salida expone la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . Si DMO es un codificador de vídeo, el PIN de salida también expone la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . En ambos casos, si DMO admite la interfaz, el PIN delega a DMO. De lo contrario, el PIN proporciona su propia implementación.

### <a name="streaming"></a>Streaming

El filtro usa la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) para controlar todos los flujos. No admite conexiones [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . El filtro llama a [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) en el DMO solo cuando recibe datos de nivel superior (incluidas las notificaciones de final de secuencia). Por lo tanto, no admite DMOs con cero flujos de entrada.

### <a name="seeking"></a>Invoca

Todas las solicitudes de búsqueda se pasan al filtro de nivel superior, a través del primer PIN de entrada en el contenedor de DMO. En el caso de DMOs de varios resultados, esto significa que el filtro de nivel superior podría recibir varias solicitudes de búsqueda cuando la aplicación busca el gráfico.

### <a name="merit"></a>Fundament

DirectShow asigna a todos los DMOs un valor de mérito predeterminado de **mérito \_ normal** + 0x800. Este valor se encuentra entre el **mérito \_ normal** y el **mérito \_ preferido**. Los filtros del descodificador generalmente tienen un valor de mérito de **mérito \_ normal**. Por lo tanto, el administrador de gráficos de filtros normalmente seleccionará un descodificador de DMO a través de un filtro de descodificador. Para reemplazar el valor predeterminado de mérito, agregue una entrada del registro a la clave del registro de DMO en el \_ CLSID raíz de las clases HKEY \_ \\ . Incluya un valor **DWORD** denominado "mérito" cuyo valor especifique el mérito.

### <a name="category"></a>Category

El filtro de contenedor de DMO no aparece solo en ninguna categoría. Cuando incluye DMO, aparece en la categoría de DirectShow que corresponde a la categoría de DMO, bajo el nombre de DMO.

### <a name="buffers"></a>Búferes

El filtro de contenedor de DMO pasa los búferes multimedia a DMO, que exponen la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

En Windows Vista o posterior, los búferes multimedia también exponen la interfaz IServiceProvider. DMO puede utilizar esta interfaz para obtener un puntero al ejemplo multimedia que está asociado con el búfer. Use el IID del identificador de servicio **\_ IMediaSample**. Un vídeo DMO puede usar la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) del ejemplo multimedia para establecer marcas de entrelazado en el ejemplo. En el código siguiente se muestra cómo obtener el puntero al ejemplo multimedia:


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Para obtener más información sobre las marcas de entrelazado por muestra, consulte la [**\_ estructura de \_ propiedades de AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Control de calidad

Si DMO expone la interfaz [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , el filtro convierte las llamadas a [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en su PIN de salida en [**IDMOQualityControl:: SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) llamadas en DMO. El parámetro *rtNow* de **SetNow** se calcula como la suma de la **marca** de tiempo y los miembros **tardíos** de la estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Usar filtro en GraphEdit

En GraphEdit, el filtro de contenedor de DMO no aparece bajo su propio nombre. En su lugar, cada DMO registrada aparece en la categoría de filtro correspondiente. Cuando agrega un DMO mediante el cuadro de diálogo **Insertar filtros** , GraphEdit crea el filtro de contenedor de DMO y lo configura para que use DMO.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Objetos multimedia de DirectX](directx-media-objects.md)
</dt> </dl>

 

 
