---
description: Capacidades de audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Capacidades de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538049"
---
# <a name="audio-capabilities"></a>Capacidades de audio

En cuanto a las capacidades de audio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devuelve una matriz de pares de estructuras de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y de [**\_ configuración de flujo de \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) . Al igual que con el vídeo, puede utilizarlo para exponer todos los tipos de funciones de audio en el PIN, como la velocidad de datos y si es compatible con mono o estéreo.

Para ver ejemplos relacionados con GetStreamCaps, consulte capacidades de [vídeo](video-capabilities.md).

Supongamos que admite el formato de onda de modulación por pulsos (PCM) (tal y como se representa en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ) en las tarifas de muestreo de 11.025, 22.050 y 44.100 muestras por segundo, todo ello en mono o estéreo de 8 o 16 bits. En este caso, se ofrecen dos pares de estructuras. El primer par tendrá una estructura de la capacidad de configuración de flujo de audio que indica que admite un mínimo de 11.025 a un máximo de 22.050 muestras por segundo con una granularidad de 11.025 muestras por segundo (la granularidad es la diferencia entre los valores admitidos). un mínimo de 8 bits a un máximo de 16 bits por muestra con una granularidad de 8 bits por muestra; y un máximo de dos canales como máximo. **\_ \_ \_** El tipo de medio del primer par sería el formato PCM predeterminado en ese intervalo, quizás 22 kilohercios (kHz), estéreo de 16 bits. El segundo par sería una funcionalidad que muestra 44.100 para las muestras mínima y máxima por segundo. bits de 8 bits (mínimo) y 16 bits (máximo) por muestra, con una granularidad de 8 bits por muestra. y un máximo de dos canales como máximo. El tipo de medio sería el formato predeterminado 44 kHz, quizás 44 kHz de 16 bits estéreo.

Si admite formatos de onda no PCM, el tipo de medio devuelto por este método puede mostrar los formatos que no son PCM que admite (con una velocidad de muestra predeterminada, una velocidad de bits y canales) y la estructura de capacidades que acompaña a ese tipo de medio puede describir qué tasas de ejemplo, velocidades de bits y canales admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Exponer los formatos de captura y compresión](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
