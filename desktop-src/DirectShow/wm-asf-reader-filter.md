---
description: Obtenga información sobre el filtro WM ASF Reader para DirectShow. Se trata de un filtro contenedor para el objeto de lector que se proporciona con el SDK Windows Media Format.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro de lector DE ASF de WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330ab870b97fc3e84ccb5b0f726d4f35ef1af147
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272620"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro de lector DE ASF de WM (DirectShow)

Wm ASF Reader es un filtro contenedor para el objeto de lector proporcionado con el Windows SDK de formato multimedia de Windows y es el filtro de origen recomendado para la reproducción de archivos de contenido basado en medios y contenido creado con cualquiera de las DDO del codificador MPEG-4 de Microsoft.



| Etiqueta | Value |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** Además, el filtro expone las siguientes interfaces del SDK de formato multimedia de Windows: [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) [**IWMReaderAdvanced,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) [**IWMReaderAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (a través de **IServiceProvider**)<br/> |
| Tipos de medios de pin de entrada                    | No aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces de pin de entrada                     | No aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de pin de salida                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IAMWMBufferPass,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) **IServiceProvider** Además, los pines exponen las siguientes interfaces del SDK de formato multimedia de Windows: **IWMStreamConfig2** (a través de **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| Filtrar CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Mérito](merit.md)                       | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Cuando se le da el nombre de un archivo ASF o una dirección URL, el lector DE ASF de WM lee el contenido comprimido, analiza las secuencias comprimidas y expone un pin de salida para cada uno. Este filtro se conecta de bajada a los filtros de códecs de audio o vídeo, que hacen la descompresión. Se admite la búsqueda si se puede buscar en el archivo ASF. El lector de ASF marca las muestras antes de enviarlas de bajada, pero no modifica las marcas de tiempo de ninguna manera.

No se admite la reproducción a velocidades diferentes de 1.0 (como se especifica en [**IMediaSeeking::SetRate).**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

Cuando el runtime del SDK de Windows Media Format envía mensajes DE ESTADO DE [**\_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) al filtro WM ASF Writer, el filtro reenvía los mensajes relacionados con la adquisición de licencias DRM como eventos [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md) Para obtener más información, vea [Reading DRM-Protected ASF Files in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

El lector DE ASF de WM implementa parcialmente las interfaces [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) e [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) con el fin de proporcionar a las aplicaciones acceso a los métodos informativos en el objeto de lector. La implementación del filtro simplemente pasa las llamadas a través de a la interfaz en el objeto de lector. Los métodos de streaming no se implementan porque el filtro debe tener un control completo sobre el proceso de streaming. Se implementan los métodos siguientes:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
