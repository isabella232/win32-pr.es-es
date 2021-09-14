---
description: Exposición de formatos de captura y compresión
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exposición de formatos de captura y compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255225"
---
# <a name="exposing-capture-and-compression-formats"></a>Exposición de formatos de captura y compresión

En este artículo se describe cómo devolver formatos de captura y compresión mediante el [**método IAMStreamConfig::GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) Este método puede obtener más información sobre los tipos de medios aceptados que la forma tradicional de enumerar los tipos de medios de un pin, por lo que normalmente se debe usar en su lugar. **GetStreamCaps puede** devolver información sobre los tipos de formatos permitidos para audio o vídeo. Además, en este artículo se proporciona código de ejemplo que muestra cómo volver a conectar la patilla de entrada de un filtro de transformación para asegurarse de que el filtro puede generar una salida determinada.

El **método GetStreamCaps** devuelve una matriz de pares de estructuras de tipo multimedia y funcionalidades. El tipo de medio es una estructura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) y las funcionalidades se representan mediante una estructura [**\_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) de CONFIGURACIÓN de SECUENCIA DE AUDIO o una estructura [**\_ \_ \_ CAPS de CONFIGURACIÓN de VIDEO STREAM.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) La primera sección de este artículo presenta un ejemplo de vídeo y la segunda presenta un ejemplo de audio.

Ese artículo contiene los siguientes temas:

-   [Funcionalidades de vídeo](video-capabilities.md)
-   [Funcionalidades de audio](audio-capabilities.md)
-   [Volver a conectar la entrada para garantizar tipos de salida específicos](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



