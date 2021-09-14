---
description: Funcionalidades de audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Funcionalidades de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162226"
---
# <a name="audio-capabilities"></a>Funcionalidades de audio

Para las funcionalidades de audio, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devuelve una matriz de pares de estructuras AM [**\_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) y [**AUDIO STREAM CONFIG \_ \_ \_ CAPS.**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Al igual que con el vídeo, puede usarlo para exponer todos los tipos de funcionalidades de audio en el pin, como la velocidad de datos y si admite mono o estéreo.

Para ver ejemplos relacionados con vídeos relacionados con GetStreamCaps, consulte [Funcionalidades de vídeo.](video-capabilities.md)

Supongamos que admite el formato de onda de pulsación de código de pulso (PCM) (tal y como se representa en la estructura [**DESATEX)**](/previous-versions/dd757713(v=vs.85)) a velocidades de muestreo de 11 025, 22 050 y 44 100 muestras por segundo, todas en mono o estéreo de 8 o 16 bits. En este caso, ofrecería dos pares de estructuras. El primer par tendría una estructura de funcionalidad **\_ \_ \_ CAPS** de CONFIGURACIÓN DE SECUENCIA DE AUDIO que dice que admite un mínimo de 11 025 hasta un máximo de 22 050 muestras por segundo con una granularidad de 11 025 muestras por segundo (granularidad es la diferencia entre los valores admitidos); un mínimo de 8 bits a un máximo de 16 bits por muestra con una granularidad de 8 bits por muestra; y un mínimo de un canal y un máximo de dos canales. El tipo de medio del primer par sería el formato PCM predeterminado en ese intervalo, quizás 22 kilohercios (kHz), estéreo de 16 bits. El segundo par sería una funcionalidad que muestra 44 100 muestras mínimas y máximas por segundo. Bits de 8 bits (mínimo) y 16 bits (máximo) por muestra, con una granularidad de 8 bits por muestra; y un mínimo de un canal y un máximo de dos canales. El tipo de medio sería el formato predeterminado de 44 kHz, quizás estéreo de 44 kHz de 16 bits.

Si admite formatos de onda que no son PCM, el tipo de medio devuelto por este método puede mostrar qué formatos no PCM admite (con una frecuencia de muestreo predeterminada, velocidad de bits y canales) y la estructura de funcionalidades que acompaña a ese tipo de medio puede describir qué otras velocidades de muestreo, velocidades de bits y canales admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Exponer los formatos de captura y compresión](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
