---
description: Reproducción de secuencias web ASF en DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Reproducción de secuencias web ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359986"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Reproducción de secuencias web ASF en DirectShow

Microsoft DirectShow admite secuencias Web en escenarios de reproducción de archivos a través del filtro de [lector ASF de WM](wm-asf-reader-filter.md) , pero debe escribir su propio filtro de DirectShow para capturar y conservar la secuencia.

> [!Note]  
> Para reproducir secuencias Web en el contenido que se transmite desde un servidor que ejecuta Windows Media Services, use el control ActiveX® de la serie Windows Media Player 9 incrustado en una página web.

 

Cuando se proporciona un archivo que contiene secuencias de tipo WMMEDIATYPE \_ FileTransfer, el lector ASF de WM creará un PIN de salida para él. El bloque de formato será una estructura de [**\_ \_ formato de Webstream de WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . (Esta estructura se documenta en la documentación del SDK de Windows Media Format). Si no hay ningún filtro de nivel inferior disponible que pueda controlar ese tipo de medio, el PIN permanecerá sin conexión, pero el archivo seguirá reproduciendo las secuencias de audio o vídeo.

Cada ejemplo multimedia de una secuencia web contiene una estructura de [**\_ encabezado de \_ ejemplo \_ WMT Webstream**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , que se documenta en la documentación del SDK de Windows Media Format. La estructura tiene una longitud variable en función de la longitud de su miembro **wszURL** . El puntero a los datos de ejemplo apunta inicialmente a esta estructura y debe avanzar el puntero más allá de la estructura para obtener acceso a los datos reales de la secuencia.

El filtro del controlador de la secuencia Web se debe basar en la clase [**CBaseRenderer**](cbaserenderer.md) . En el método [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , el filtro deberá analizar la estructura para obtener información sobre la secuencia web y, a continuación, realizar la acción adecuada. Normalmente, esto implicará guardar el archivo en el disco y, a continuación, llamar a las funciones [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) y [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) o [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) para colocar los archivos en la memoria caché de Internet Explorer. El filtro debe administrar los archivos de varias partes, es decir, los archivos que son más grandes que un ejemplo y también debe controlar los comandos de representación, que se especifican en el miembro **\_ Header de ejemplo Webstream de WMT \_ \_ . wSampleType** . El filtro envía un evento de [**\_ \_ evento OLE de EC**](ec-ole-event.md) a la aplicación, junto con el texto de la cadena de **ejemplo de \_ Webstream \_ \_ . wszURL de WMT** que contiene el nombre del archivo que se va a representar. A continuación, la aplicación hace que el explorador muestre la página especificada. Si la secuencia Web se ha creado correctamente, el archivo ya debe estar en la memoria caché.

Para obtener más información sobre \_ el formato de WEBstream de WMT \_ y \_ el encabezado de ejemplo de Webstream WMT \_ \_ , vea la documentación del SDK de Windows Media Format.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
