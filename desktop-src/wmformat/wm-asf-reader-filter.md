---
title: Filtro de lector de ASF de WM (Windows Media Format SDK 11)
description: Obtenga información sobre el filtro wm asf Reader.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,WM ASF Reader
- DirectShow,WM ASF Reader
- Filtros QASF, Lector DE ASF de WM
- Lector de ASF de WM
- Advanced Systems Format (ASF),WM ASF Reader
- ASF (formato de sistemas avanzados), LECTOR DE ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444286"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtro de lector de ASF de WM (Windows Media Format SDK 11)

Cuando se le da el nombre de un archivo ASF o una dirección URL, el lector de ASF wm lee el contenido comprimido, analiza las secuencias y expone un pin de salida para cada uno. Este filtro se conecta de bajada a la Windows Media Audio o Windows Media Video, que hacen la descompresión. Se admite la búsqueda si se puede buscar en el archivo ASF. El lector de ASF de WM aplica marcas de tiempo a los ejemplos de medios en función de la marca de tiempo del archivo ASF, pero no modifica las marcas de tiempo de ninguna manera. Internamente, el filtro usa el Windows Media Format lector para leer el contenido basado en Windows Media.

> [!Note]  
> En el SDK de DirectX, este filtro no es el filtro de origen predeterminado para los archivos ASF, por lo que con ese SDK no se puede usar este filtro con el **método RenderFile.** debe agregarlo explícitamente al gráfico de filtros mediante su identificador de clase (CLSID). Este comportamiento es diferente con Windows Media Format SDK. Al instalar las bibliotecas en tiempo de Windows Media Format SDK, el lector de ASF de WM se registra como filtro predeterminado para los archivos ASF.

 

La tabla siguiente contiene información sobre el filtro lector de ASF de WM, como las interfaces y los tipos de medios que admite.



|  Filtrar información                      |  Tipos                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IBaseFilter,** **IFileSourceFilter,** **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementado parcialmente. Vea Remarks.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (a través **de IServiceProvider**) |
| Tipos de medios de pin de entrada  | No aplicable                                                                                                                                                                                                                                |
| Interfaces de pin de entrada   | No aplicable                                                                                                                                                                                                                                |
| Tipos de medios de pin de salida | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                         |
| Tipo de formato            | **VIDEOINFOHEADER2 si** el contenido está [*entrelazado; de*](wmformat-glossary.md)lo **contrario, VIDEOINFOHEADER**                                                                                                                    |
| Interfaces de pin de salida  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (a **través de IServiceProvider**)                                                                                                                             |
| Filtrar CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID de la página de propiedades    | Ninguna página de propiedades                                                                                                                                                                                                                              |
| Executable             | Qasf.dll                                                                                                                                                                                                                                      |
| Mérito                  | NO PROBABLE \_ QUE SE PRODUZCAN LOS CASO                                                                                                                                                                                                                               |
| Categoría de filtro        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

El Lector de ASF de WM implementa parcialmente las interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** con el fin de proporcionar a las aplicaciones acceso a los métodos informativos en el objeto de lector. La implementación del filtro simplemente pasa las llamadas a través de a la interfaz en el objeto de lector. Los métodos de streaming no se implementan porque el filtro debe tener un control completo sobre el proceso de streaming. Se implementan **los métodos IWMReaderAdvanced** e **IWMReaderAdvanced2** siguientes:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lectura de archivos ASF en DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




