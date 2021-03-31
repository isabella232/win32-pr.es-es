---
description: Exponer los formatos de captura y compresión
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exponer los formatos de captura y compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806878"
---
# <a name="exposing-capture-and-compression-formats"></a>Exponer los formatos de captura y compresión

En este artículo se describe cómo devolver los formatos de captura y compresión mediante el método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Este método puede obtener más información sobre los tipos de medios aceptados que la manera tradicional de enumerar los tipos de medios de un PIN, por lo que normalmente se debe usar en su lugar. **GetStreamCaps** puede devolver información sobre los tipos de formatos permitidos para audio o vídeo. Además, en este artículo se proporciona código de ejemplo que muestra cómo volver a conectar la clavija de entrada de un filtro de transformación para asegurarse de que el filtro puede generar una salida determinada.

El método **GetStreamCaps** devuelve una matriz de pares de estructuras de tipo de medio y funcionalidad. El tipo de medio es una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y las funciones se representan mediante una estructura de [**audio de \_ flujo \_ \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) de vídeo o una estructura de Cap de configuración de [**flujo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . La primera sección de este artículo presenta un ejemplo de vídeo y el segundo presenta un ejemplo de audio.

Ese artículo contiene los siguientes temas:

-   [Capacidades de vídeo](video-capabilities.md)
-   [Capacidades de audio](audio-capabilities.md)
-   [Volver a conectar la entrada para garantizar tipos de salida específicos](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



