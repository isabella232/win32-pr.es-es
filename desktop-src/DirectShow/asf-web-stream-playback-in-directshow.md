---
description: Reproducción de secuencias web de ASF en DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Reproducción de secuencias web de ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28d9d3b7ea4fba5537383a846e6eff64f3815eefa21613c6056a15a5e497f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824630"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Reproducción de secuencias web de ASF en DirectShow

Microsoft DirectShow admite secuencias web en escenarios de reproducción de archivos mediante el filtro [lector de ASF](wm-asf-reader-filter.md) wm, pero debe escribir su propio filtro DirectShow para capturar y conservar la secuencia.

> [!Note]  
> Para reproducir secuencias web en contenido que se transmite desde un servidor que ejecuta Servicios de Windows Media, use el control Reproductor de Windows Media serie 9 ActiveX® insertado en una página web.

 

Cuando se le da un archivo que contiene secuencias de tipo WMMEDIATYPE FileTransfer, el lector DE ASF de WM creará un pin \_ de salida para él. El bloque de formato será una [**estructura \_ WMT WEBSTREAM \_ FORMAT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) (Esta estructura se documenta en la documentación del SDK Windows Media Format). Si no hay ningún filtro de bajada disponible que pueda controlar ese tipo de medio, el pin permanecerá desconectado, pero el archivo seguirá reproduce las secuencias de audio o vídeo.

Cada ejemplo multimedia de una secuencia web contiene una estructura DE ENCABEZADO DE EJEMPLO DE [**WMT \_ WEBSTREAM, \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) que se documenta en la documentación del SDK Windows Media Format. La estructura tiene una longitud variable en función de la longitud de su **miembro wszURL.** El puntero a los datos de ejemplo apunta inicialmente a esta estructura y debe avanzar el puntero más allá de la estructura para tener acceso a los datos reales de la secuencia.

El filtro del controlador de flujo web debe basarse en la [**clase CBaseRenderer.**](cbaserenderer.md) En el [**método CBaseRenderer::D oRenderSample,**](cbaserenderer-dorendersample.md) el filtro deberá analizar la estructura para obtener información sobre la secuencia web y, a continuación, realizar la acción adecuada. Normalmente, esto implicará guardar el archivo en el disco y, a continuación, llamar a las funciones [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) y [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) o [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) para colocar los archivos en la caché de Internet Explorer. El filtro debe controlar los archivos de varias partes, es decir, los archivos que son mayores que un ejemplo, y también debe controlar los comandos de representación, especificados por el miembro **WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER.wSampleType.** El filtro envía un evento [**\_ EC OLE \_ EVENT**](ec-ole-event.md) a la aplicación, junto con el texto de la cadena **WMT \_ WEBSTREAM SAMPLE \_ \_ HEADER.wszURL** que contiene el nombre del archivo que se va a representar. A continuación, la aplicación hace que el explorador muestre la página especificada. Si la secuencia web se ha escrito correctamente, el archivo ya debe estar en la memoria caché.

Para obtener más información sobre WMT WEBSTREAM FORMAT y \_ \_ WMT \_ WEBSTREAM SAMPLE HEADER, consulte la documentación Windows \_ SDK de formato \_ multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
