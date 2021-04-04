---
description: En esta sección se describe cómo usar la API de Transcode para volver a codificar los archivos multimedia. La API de transcodificación se presentó en Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908637"
---
# <a name="transcode-api"></a>API de transcodificación

En esta sección se describe cómo usar la API de Transcode para volver a codificar los archivos multimedia. La API de transcodificación se presentó en Windows 7.

La *transcodificación* es la conversión de un archivo multimedia digital de un formato a otro. La API de Transcode está diseñada para usarse con la [sesión multimedia](media-session.md). Simplifica el uso de la sesión multimedia para determinados tipos de aplicaciones de transcodificación:

-   Codificación de velocidad de bits constante (CBR), donde la velocidad de bits de destino se conoce de antemano.
-   Como máximo, una secuencia de audio y otra de vídeo.
-   Codificación de y a un archivo.

La API de Transcode no admite lo siguiente:

-   Velocidad de bits variable (VBR) o codificación de múltiples pasadas.
-   Varias secuencias de audio o varias secuencias de vídeo.
-   Contenido protegido con DRM que no sea archivos ASF protegidos con WMDRM.
-   Streaming en vivo, como streaming de Live-to-file o streaming en vivo.

Si la aplicación de codificación encaja dentro de estas restricciones, la API de Transcode es un modelo de programación más sencillo que el uso de la sesión multimedia por sí solo.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la API de Transcode](about-the-transcode-api.md)<br/>                              | Proporciona información general sobre la API de Transcode.<br/>                                                                                                                                                                |
| [Uso de la API de Transcode](fast-transcode-objects.md)<br/>                               | Describe cómo una aplicación utiliza la API de Transcode.<br/>                                                                                                                                                             |
| [Tutorial: codificación de un archivo MP4](tutorial--encoding-an-mp4-file-.md)<br/>               | Un tutorial paso a paso que muestra cómo usar la API de Transcode para codificar un archivo MP4.<br/>                                                                                                                           |
| [Tutorial: codificar un archivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Muestra cómo usar la API de Transcode para codificar un archivo WMA. En este tutorial se modifica el código que se muestra en [Tutorial: codificar un archivo MP4](tutorial--encoding-an-mp4-file-.md), por lo que primero debe leer ese tutorial.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Información general de la codificación en Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




