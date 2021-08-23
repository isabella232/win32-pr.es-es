---
description: Exposición de los formatos de captura y compresión
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exposición de los formatos de captura y compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80821ade82b894a7c3e2752528ffdd72bc2223a4616b629f7e2b236461b31e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685745"
---
# <a name="exposing-capture-and-compression-formats"></a>Exposición de los formatos de captura y compresión

En este artículo se describe cómo devolver formatos de captura y compresión mediante el [**método IAMStreamConfig::GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) Este método puede obtener más información sobre los tipos de medios aceptados que la forma tradicional de enumerar los tipos multimedia de un pin, por lo que normalmente se debe usar en su lugar. **GetStreamCaps puede** devolver información sobre los tipos de formatos permitidos para audio o vídeo. Además, en este artículo se proporciona código de ejemplo que muestra cómo volver a conectar la clavija de entrada de un filtro de transformación para asegurarse de que el filtro puede generar una salida determinada.

El **método GetStreamCaps** devuelve una matriz de pares de estructuras de tipo de medio y funcionalidades. El tipo de medio es una estructura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) y las funcionalidades se representan mediante una estructura [**\_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) de CONFIGURACIÓN de SECUENCIA DE AUDIO o una estructura [**\_ \_ \_ CAPS de CONFIGURACIÓN de VIDEO STREAM.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) La primera sección de este artículo presenta un ejemplo de vídeo y la segunda presenta un ejemplo de audio.

Ese artículo contiene los siguientes temas:

-   [Funcionalidades de vídeo](video-capabilities.md)
-   [Funcionalidades de audio](audio-capabilities.md)
-   [Volver a conectar la entrada para garantizar tipos de salida específicos](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



