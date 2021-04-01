---
title: Filtro de lector ASF de WM (Windows Media Format 11 SDK)
description: Filtro de lector ASF de WM
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- SDK de Windows Media Format, lector ASF de WM
- DirectShow, lector ASF de WM
- Filtros QASF, lector ASF de WM
- Lector ASF de WM
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (formato de sistemas avanzados), lector ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800686"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtro de lector ASF de WM (Windows Media Format 11 SDK)

Cuando se proporciona el nombre de un archivo ASF o una dirección URL, el lector ASF de WM lee el contenido comprimido, analiza los flujos y expone un PIN de salida para cada uno de ellos. Este filtro conecta el nivel inferior al Windows Media Audio o Windows Media Video DMOs, que realizan la descompresión. La búsqueda se admite si se puede buscar en el archivo ASF. El lector ASF de WM aplica las marcas de tiempo a los ejemplos de medios en función de la marca de tiempo del archivo ASF, pero no modifica las marcas de tiempo de ningún modo. Internamente, el filtro utiliza el objeto lector de formato de Windows Media para leer el contenido basado en Windows Media.

> [!Note]  
> En el SDK de DirectX, este filtro no es el filtro de origen predeterminado para los archivos ASF, por lo que con ese SDK no puede usar este filtro con el método **RenderFile** ; debe agregarlo explícitamente al gráfico de filtros mediante su identificador de clase (CLSID). Este comportamiento es diferente con el SDK de Windows Media Format. Al instalar las bibliotecas en tiempo de ejecución del SDK de Windows Media Format, el lector ASF de WM se registra como filtro predeterminado para los archivos ASF.

 

La tabla siguiente contiene información sobre el filtro de lector ASF de WM, como las interfaces y los tipos de medios que admite.



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementado parcialmente). Vea la sección Comentarios.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (a través de **IServiceProvider**) |
| Tipos de medios de anclaje de entrada  | No aplicable                                                                                                                                                                                                                                |
| Interfaces de PIN de entrada   | No aplicable                                                                                                                                                                                                                                |
| Tipos de medios de anclaje de salida | MEDIATYPE \_ vídeo, mediatype \_ audio, mediatype \_ comando, mediatype \_ FileTransfer                                                                                                                                                         |
| Tipo de formato            | **VIDEOINFOHEADER2** si el contenido está [*entrelazado*](wmformat-glossary.md); de lo contrario, **VIDEOINFOHEADER**                                                                                                                    |
| Interfaces de clavija de salida  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (a través de **IServiceProvider**)                                                                                                                             |
| Identificador CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID de la página de propiedades    | Ninguna página de propiedades                                                                                                                                                                                                                              |
| Executable             | Qasf.dll                                                                                                                                                                                                                                      |
| Fundament                  | MÉRITO \_ improbable                                                                                                                                                                                                                               |
| Categoría de filtro        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

El lector ASF de WM implementa parcialmente las interfaces **IWMReaderAdvanced** y **IWMReaderAdvanced2** para proporcionar a las aplicaciones acceso a los métodos informativos del objeto lector. La implementación del filtro simplemente pasa las llamadas a la interfaz en el objeto del lector. Los métodos de transmisión por secuencias no se implementan porque el filtro debe tener control total sobre el proceso de streaming. Se implementan los siguientes métodos **IWMReaderAdvanced** y **IWMReaderAdvanced2** :

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de QASF de DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Leer archivos ASF en DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




