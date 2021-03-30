---
title: Reproducción de secuencias Web en DirectShow
description: Reproducción de secuencias Web en DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, reproducción de secuencias Web
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), reproducción de secuencias Web
- ASF (formato de sistemas avanzados), reproducción de secuencias Web
- DirectShow, reproducción de secuencias Web
- Secuencias Web, DirectShow
- Secuencias Web, reproducción en DirectShow
- secuencias, reproducción de secuencias Web en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994049"
---
# <a name="web-stream-playback-in-directshow"></a>Reproducción de secuencias Web en DirectShow

Microsoft DirectShow admite secuencias web (consulte [secuencias web](web-streams.md) para obtener más información) en escenarios de reproducción de archivos mediante el filtro de [lector ASF de WM](wm-asf-reader-filter.md) , pero debe escribir su propio filtro de DirectShow para capturar y conservar la secuencia.

> [!Note]  
> Para reproducir secuencias Web en el contenido que se transmite desde un servidor que ejecuta Windows Media Services, use el control ActiveX® de la serie Windows Media Player 9 incrustado en una página web.

 

Cuando se proporciona un archivo que contiene secuencias de tipo WMMEDIATYPE \_ FileTransfer, el lector ASF de WM creará un PIN de salida para él. El bloque de formato será una estructura de [**\_ \_ formato de Webstream de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . Si no hay ningún filtro de nivel inferior disponible que pueda controlar ese tipo de medio, el PIN permanecerá sin conexión, pero el archivo seguirá reproduciendo las secuencias de audio o vídeo.

Es importante comprender que cada ejemplo multimedia de una secuencia web contiene una estructura de [**\_ \_ \_ encabezado de ejemplo WMT Webstream**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , que tiene una longitud variable en función de la longitud de su miembro **wszURL** . El puntero a los datos de ejemplo apunta inicialmente a esta estructura y debe avanzar el puntero más allá de la estructura para obtener acceso a los datos reales de la secuencia. El filtro del controlador de la secuencia Web se debe basar en la clase **CBaseRenderer** . En el método **DoRenderSample** , el filtro deberá analizar la estructura para obtener información sobre la secuencia web y, a continuación, realizar la acción adecuada. Normalmente, esto implicará guardar el archivo en el disco y, a continuación, llamar a **CommitUrlCacheEntry** y **CreateUrlCacheEntry** para colocar los archivos en la memoria caché de Internet Explorer. El filtro debe administrar los archivos de varias partes, es decir, los archivos que son más grandes que un ejemplo y también debe controlar los comandos de representación, que se especifican en el miembro **\_ Header de ejemplo Webstream de WMT \_ \_ . wSampleType** . El filtro envía un **\_ \_ evento OLE de EC** a la aplicación, junto con el texto de la cadena de ejemplo de **\_ Webstream \_ \_ . wszURL de WMT** que contiene el nombre del archivo que se va a representar. A continuación, la aplicación hace que el explorador muestre la página especificada. Si la secuencia Web se ha creado correctamente, el archivo ya debe estar en la memoria caché.

Para obtener más información sobre los **\_ \_ eventos OLE** **CBaseRenderer**, **DoRenderSample** y EC, vea la documentación del SDK de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Secuencias Web**](web-streams.md)
</dt> </dl>

 

 




