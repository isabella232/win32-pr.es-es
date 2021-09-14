---
description: DMO Filtro de contenedor
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO Filtro de contenedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375235"
---
# <a name="dmo-wrapper-filter"></a>DMO Filtro de contenedor

El filtro DMO wrapper permite que una aplicación DirectShow use un objeto multimedia [DirectX](directx-media-objects.md) (DMO) dentro de un gráfico de filtros. El filtro ajusta el DMO controla todos los detalles del uso de la DMO, como pasar datos hacia y desde el DMO. Además, el filtro agrega el DMO, por lo que la aplicación puede consultar el filtro para cualquier interfaz COM que el DMO expone.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipos de medios de pin de entrada                    | Consulte Comentarios                                                                                                                                                                                                                                        |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de pin de salida                   | Consulte Comentarios                                                                                                                                                                                                                                        |
| Interfaces de pin de salida                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                   |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Mérito](merit.md)                       | Consulte Comentarios                                                                                                                                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | Consulte Comentarios                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

### <a name="limitations"></a>Limitaciones

El DMO contenedor tiene las siguientes limitaciones:

-   No admite DDO con cero entradas, varias entradas o cero salidas. (Admite DDO con una entrada y varias salidas).
-   No admite transportes personalizados. Todo el transporte de datos se realiza a través de [**la interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   No usa la **interfaz IMediaObjectInPlace;** todo el procesamiento se realiza mediante [**métodos IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)

### <a name="pins"></a>Chinchetas

Para cada flujo de entrada del DMO, el filtro crea un pin de entrada correspondiente. Para cada flujo de salida, crea un pin de salida correspondiente. Los tipos de medios que admite cada pin dependen del DMO

### <a name="encoder-interfaces"></a>Interfaces de codificador

Si el DMO es un codificador de vídeo o un codificador de audio, el pin de salida expone la [**interfaz IAMStreamConfig.**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) Si el DMO es un codificador de vídeo, el pin de salida también expone la [**interfaz IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) En ambos casos, si el DMO admite la interfaz , el pin delega en el DMO. De lo contrario, el pin proporciona su propia implementación.

### <a name="streaming"></a>Streaming

El filtro usa la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) para controlar todo el streaming. No admite conexiones [**IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) El filtro llama [**a IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) en el DMO solo cuando recibe datos de nivel superior (incluidas las notificaciones de fin de flujo). Por lo tanto, no admite DDO con cero flujos de entrada.

### <a name="seeking"></a>Buscando

Todas las solicitudes de búsqueda se pasan al filtro ascendente, a través de la primera patilla de entrada del DMO contenedor. En el caso de las DDO de varias salidas, esto significa que el filtro ascendente podría recibir varias solicitudes de búsqueda cuando la aplicación busca el gráfico.

### <a name="merit"></a>Mérito

DirectShow asigna a todas las DDO un valor de merececión predeterminado **de NORMAL + \_** 0x800. Este valor se encuentra entre **LO \_ NORMAL y** **\_ PREFERITORIO PREFERIDO.** Por lo general, los filtros descodificadores tienen un valor de **meritorio de LO \_ NORMAL.** Por lo tanto, el administrador de gráficos de filtro normalmente seleccionará un descodificador DMO un filtro descodificador. Para invalidar el valor predeterminado de los privilegios, agregue una entrada del Registro a la DMO del Registro de HKEY \_ CLASSES \_ ROOT \\ CLSID. Incluya un **valor DWORD** denominado "Honor", cuyo valor especifica el valor.

### <a name="category"></a>Category

El DMO wrapper no aparece por sí solo en ninguna categoría. Cuando encapsula un DMO, aparece en la categoría DirectShow correspondiente a la categoría del DMO, bajo el nombre del DMO.

### <a name="buffers"></a>Búferes

El DMO wrapper pasa búferes multimedia al DMO que exponen la [**interfaz IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer)

En Windows Vista o versiones posteriores, los búferes multimedia también exponen la interfaz IServiceProvider. El DMO puede usar esta interfaz para obtener un puntero al ejemplo multimedia asociado al búfer. Use el identificador de **servicio IID \_ IMediaSample**. Un vídeo DMO puede usar la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) del ejemplo multimedia para establecer marcas de interlace en el ejemplo. El código siguiente muestra cómo obtener el puntero al ejemplo multimedia:


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



Para obtener más información sobre las marcas de intercalación por ejemplo, vea [**AM \_ SAMPLE2 \_ PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Control de calidad

Si el DMO expone la interfaz [**IDMOQualityControl,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) el filtro convierte las llamadas [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en su pin de salida en [**llamadas IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) en el DMO. El *parámetro rtNow* de **SetNow** se calcula como la suma de los **miembros TimeStamp** y **Late** de la [**estructura Quality.**](/windows/win32/api/strmif/ns-strmif-quality)

### <a name="using-the-fiter-in-graphedit"></a>Uso de Fiter en GraphEdit

En GraphEdit, el filtro DMO wrapper no aparece bajo su propio nombre. En su lugar, cada DMO registrado aparece en la categoría de filtro adecuada. Cuando se agrega un DMO  a través del cuadro de diálogo Insertar filtros, GraphEdit crea el filtro DMO Wrapper y lo configura para usar ese DMO.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Objetos multimedia de DirectX](directx-media-objects.md)
</dt> </dl>

 

 
