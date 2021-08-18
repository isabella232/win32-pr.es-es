---
description: En este tema se describe el volumen XAudio2 y el control de inclinación.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Control de volumen y tono de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6376ad599b496a640b49d7eb539e1da774e31c71a3bf2a8e0c863fc140e19b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962494"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Control de volumen y tono de XAudio2

En este tema se describe el volumen XAudio2 y el control de inclinación.

## <a name="volume-control"></a>Control de volumen

Los niveles de volumen se expresan como multiplicadores de amplitud de punto flotante entre -XAUDIO2 MAX VOLUME LEVEL y \_ \_ \_ XAUDIO2 \_ MAX VOLUME LEVEL \_ \_ (-224 a 224), con una ganancia máxima de 144,5 dB. Un volumen de 1,0 significa que no hay atenuación ni ganancia; 0 significa silencio; y los niveles negativos se pueden usar para invertir la fase del audio. En XAudio2.h se proporcionan dos funciones insertadas para convertir entre unidades de volumen: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) y [**XAudio2AmplitudeRatioToDecibels.**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)

Puede aplicar un nivel de volumen al audio en varios puntos a medida que fluye a través del gráfico XAudio2:

-   Todos los tipos de voz aplican un nivel de volumen general a su entrada, que controlan mediante el método [**IXAudio2Voice::SetVolume.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) En las voces de submezcla y mastering, el nivel de volumen general se aplica justo antes de la cadena de filtro y efecto integrada de la voz. En las voces de origen, el nivel de volumen general se aplica después de la cadena de filtro y efecto integrada de la voz.
-   Las voces aplican un nivel de volumen por canal a su salida, que controlan mediante el método [**IXAudio2Voice::SetChannelVolumes.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) El nivel de volumen por canal se aplica justo después de la conversión de frecuencia de muestreo final de la voz y antes de que se envíe a otras voces.
-   Cada conexión entre una voz y otra tiene una tabla de niveles que se usa para enviar audio desde cada canal de origen a cada canal de destino, que se controla mediante el método [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)

Todos los volúmenes generales y los volúmenes de canal tienen como valor predeterminado 1.0 inicialmente. Todas las matrices de nivel de envío tienen como valor predeterminado los valores adecuados que conservan la potencia de señal y el posicionamiento del canal con la mayor precisión posible. Consulte la introducción a [la asignación de canales predeterminada de XAudio2](xaudio2-default-channel-mapping.md) para obtener más información.

> [!Note]  
> XAudio2 ajusta automáticamente los niveles de volumen en función de la configuración del hablante del usuario para mantener un nivel de volumen coherente entre configuraciones. Si la configuración del usuario no coincide con su configuración física, el volumen será demasiado alto o demasiado suave en comparación con un sistema con una configuración precisa. Por ejemplo, un sistema configurado para 5.1 rodeará los altavoces de sonido que solo tienen dos altavoces conectados sonará demasiado suave. XAudio2 no puede detectar si la configuración del hablante del usuario coincide correctamente con su configuración física.

 

## <a name="pitch-control"></a>Pitch Control

Los lanzamientos se expresan como relaciones de velocidad de entrada/salida entre 1/1024 y 1024/1, ambos incluidos. Una proporción de 1/1024 reduce el tono en 10 octaves, mientras que una proporción de 1024/1 lo eleva en 10 octágras. Solo puede usar el método [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar ajustes de tono a las voces de origen y solo si no se crearon con la marca XAUDIO2 \_ VOICE \_ NOPITCH. La relación de frecuencia predeterminada es 1/1: es decir, sin cambio de tono. En XAudio2.h se proporcionan dos funciones insertadas para convertir entre las relaciones de frecuencia y las semirraciones: [**XAudio2FrequencyRatioToSemitio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) y [**XAudio2SemilinoToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de volumen y tono](volume-and-pitch-control.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: Cambiar el tono de voz](how-to--change-voice-pitch.md)
</dt> <dt>

[Cómo: Cambiar el volumen de voz](how-to--change-voice-volume.md)
</dt> </dl>

 

 
