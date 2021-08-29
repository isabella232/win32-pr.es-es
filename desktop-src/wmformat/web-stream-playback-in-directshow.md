---
title: Reproducción de Secuencia web en DirectShow
description: Reproducción de Secuencia web en DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, reproducción de secuencias web
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Formato de sistemas avanzados (ASF), reproducción de secuencias web
- ASF (formato de sistemas avanzados), reproducción de secuencias web
- DirectShow, reproducción de secuencias web
- Flujos web, DirectShow
- Secuencias web, reproducción en DirectShow
- streams,Web stream playback in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10d70b4c6958881f3a49544e8119163ad68ef12d6b127ca1af144a1036def8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431982"
---
# <a name="web-stream-playback-in-directshow"></a>Reproducción de Secuencia web en DirectShow

Microsoft DirectShow admite secuencias web (consulte [Web Secuencias](web-streams.md) para obtener más información) en escenarios de reproducción de archivos a través del filtro [wm ASF Reader,](wm-asf-reader-filter.md) pero debe escribir su propio filtro DirectShow para capturar y conservar la secuencia.

> [!Note]  
> Para reproducir secuencias web en contenido que se transmite desde un servidor que ejecuta Servicios de Windows Media, use el control Reproductor de Windows Media serie 9 ActiveX® insertado en una página web.

 

Cuando se le da un archivo que contiene secuencias de tipo WMMEDIATYPE FileTransfer, el lector DE ASF de WM creará un pin \_ de salida para él. El bloque de formato será una [**estructura \_ WMT WEBSTREAM \_ FORMAT.**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Si no hay ningún filtro de bajada disponible que pueda controlar ese tipo de medio, el pin permanecerá sin conectar, pero el archivo seguirá reprodectado las secuencias de audio o vídeo.

Es importante comprender que cada ejemplo multimedia de un flujo web contiene una estructura DE ENCABEZADO DE EJEMPLO [**DE WMT \_ WEBSTREAM, \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) que tiene una longitud variable en función de la longitud de su **miembro wszURL.** El puntero a los datos de ejemplo apunta inicialmente a esta estructura y debe avanzar el puntero más allá de la estructura para tener acceso a los datos reales de la secuencia. El filtro del controlador de flujo web debe basarse en la **clase CBaseRenderer.** En el **método DoRenderSample,** el filtro deberá analizar la estructura para obtener información sobre la secuencia web y, a continuación, realizar la acción adecuada. Normalmente, esto implicará guardar el archivo en el disco y, a continuación, llamar a **CommitUrlCacheEntry** y **CreateUrlCacheEntry** para colocar los archivos en la caché Internet Explorer datos. El filtro debe controlar los archivos de varias partes, es decir, los archivos que son mayores que un ejemplo, y también debe controlar los comandos de representación, especificados por el miembro **WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER.wSampleType.** El filtro envía un EVENTO **\_ OLE \_ DE EC** a la aplicación, junto con el texto de la cadena **WMT \_ WEBSTREAM SAMPLE \_ \_ HEADER.wszURL** que contiene el nombre del archivo que se va a representar. A continuación, la aplicación hace que el explorador muestre la página especificada. Si la secuencia web se ha escrito correctamente, el archivo ya debe estar en la memoria caché.

Para obtener más información **sobre CBaseRenderer,** **DoRenderSample** y **EC OLE \_ \_ EVENT**, vea la documentación DirectShow SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Web Secuencias**](web-streams.md)
</dt> </dl>

 

 




