---
description: En esta sección se describe cómo usar la API de transcodificación para volver a codificar los archivos multimedia. La API de transcodificación se introdujo en Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: Transcodificación de API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268695"
---
# <a name="transcode-api"></a>Transcodificación de API

En esta sección se describe cómo usar la API de transcodificación para volver a codificar los archivos multimedia. La API de transcodificación se introdujo en Windows 7.

*La transcodificación* es la conversión de un archivo multimedia digital de un formato a otro. La API de transcodificación está diseñada para usarse con la [sesión multimedia](media-session.md). Simplifica el uso de la sesión multimedia para determinados tipos de aplicaciones de transcodificación:

-   Codificación de velocidad de bits constante (CBR), donde la velocidad de bits de destino se conoce de antemano.
-   Como máximo, una secuencia de audio y una secuencia de vídeo.
-   Codificación desde y hacia un archivo.

Transcode API no admite lo siguiente:

-   Velocidad de bits variable (VBR) o codificación de varios pases.
-   Varias secuencias de audio o varias secuencias de vídeo.
-   Contenido protegido con DRM distinto de los archivos ASF protegidos con WMDRM.
-   Streaming en vivo, como streaming en vivo a archivo o streaming de live-to-live.

Si la aplicación de codificación se ajusta a estas restricciones, la API de transcodificación es un modelo de programación más sencillo que usar solo la sesión multimedia.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de Transcode API](about-the-transcode-api.md)<br/>                              | Proporciona información general sobre la API de transcodificación.<br/>                                                                                                                                                                |
| [Uso de Transcode API](fast-transcode-objects.md)<br/>                               | Describe cómo una aplicación usa la API de transcodificación.<br/>                                                                                                                                                             |
| [Tutorial: Codificación de un archivo MP4](tutorial--encoding-an-mp4-file-.md)<br/>               | Tutorial paso a paso que muestra cómo usar la API de transcodificación para codificar un archivo MP4.<br/>                                                                                                                           |
| [Tutorial: Codificación de un archivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Muestra cómo usar la API de transcodificación para codificar un archivo WMA. En este tutorial se modifica el código que se muestra [en Tutorial: Codificación](tutorial--encoding-an-mp4-file-.md)de un archivo MP4, por lo que primero debe leer ese tutorial.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Información general sobre la codificación en Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




