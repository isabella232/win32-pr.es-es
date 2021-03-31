---
description: Filtro de lector ASF de WM
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro de lector ASF de WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df563667ed614a238e8fb31e08a2d71c721c2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277196"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro de lector ASF de WM (DirectShow)

El lector ASF de WM es un filtro de contenedor para el objeto lector que se proporciona con el SDK de Windows Media Format y es el filtro de origen recomendado para la reproducción de archivos de contenido basado en Windows Media y el contenido creado con cualquiera de los DMOs del codificador MPEG-4 de Microsoft.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** además, el filtro expone las siguientes interfaces del SDK de Windows Media Format: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (a través de **IServiceProvider**)<br/> |
| Tipos de medios de anclaje de entrada                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces de PIN de entrada                     | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ vídeo, mediatype \_ audio, mediatype \_ comando, mediatype \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de clavija de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** además, las clavijas exponen las siguientes interfaces del SDK de Windows Media Format: **IWMStreamConfig2** (a través de **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| Identificador CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Cuando se proporciona el nombre de un archivo ASF o una dirección URL, el lector ASF de WM lee el contenido comprimido, analiza los flujos comprimidos y expone un PIN de salida para cada uno de ellos. Este filtro conecta los filtros de nivel inferior a audio y/o códecs de vídeo, que realizan la descompresión. La búsqueda se admite si se puede buscar en el archivo ASF. La hora del lector ASF marca los ejemplos antes de enviarlos a la baja, pero no modifica las marcas de tiempo de ningún modo.

No se admite la reproducción a velocidades distintas de 1,0 (tal y como se especifica en [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)).

Cuando el tiempo de ejecución del SDK de Windows Media Format envía mensajes de [**\_ Estado WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) al filtro de escritor ASF de WM, el filtro reenvía los mensajes relacionados con la adquisición de licencias DRM como eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) . Para obtener más información, vea [leer DRM-Protected archivos ASF en DirectShow](reading-drm-protected-asf-files-in-directshow.md).

El lector ASF de WM implementa parcialmente las interfaces [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) y [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) para proporcionar a las aplicaciones acceso a los métodos informativos del objeto lector. La implementación del filtro simplemente pasa las llamadas a la interfaz en el objeto del lector. Los métodos de transmisión por secuencias no se implementan porque el filtro debe tener control total sobre el proceso de streaming. Se implementan los métodos siguientes:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
