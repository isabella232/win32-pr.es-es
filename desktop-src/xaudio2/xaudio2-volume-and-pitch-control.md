---
description: En este tema se describe el control de volumen y de paso de XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Volumen y control de paso de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277755"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Volumen y control de paso de XAudio2

En este tema se describe el control de volumen y de paso de XAudio2.

## <a name="volume-control"></a>Control de volumen

Los niveles de volumen se expresan como multiplicadores de amplitud de punto flotante entre-XAUDIO2 \_ Max de \_ nivel de volumen \_ y \_ \_ nivel máximo \_ de volumen de xaudio2 (de-224 a 224), con una ganancia máxima de 144,5 dB. Un volumen de 1,0 significa que no hay atenuación ni ganancia; 0 significa silencio; y los niveles negativos se pueden usar para invertir la fase del audio. En XAudio2. h se proporcionan dos funciones insertadas para realizar conversiones entre unidades de volumen: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) y [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

Puede aplicar un nivel de volumen al audio en varios puntos a medida que fluye a través del gráfico de XAudio2:

-   Todos los tipos de voz aplican un nivel de volumen general a su entrada, que controlan mediante el método [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) . En las voces de submezcla y de maestro, el nivel de volumen global se aplica justo antes de la cadena de filtro y efecto integrados de la voz. En las voces de origen, el nivel de volumen general se aplica después de la cadena de filtro y efecto integrados de la voz.
-   Las voces aplican un nivel de volumen por canal a su salida, que controlan mediante el método [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) . El nivel de volumen por canal se aplica justo después de la conversión final de la frecuencia de muestreo de la voz y antes de que se envíe a otras voces.
-   Cada conexión entre una voz y otra tiene una tabla de niveles que se usa para enviar audio desde cada canal de origen a cada canal de destino, que se controla mediante el método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .

Todos los volúmenes generales y volúmenes de canales tienen como valor predeterminado 1,0 inicialmente. Todas las matrices de nivel de envío tienen como valor predeterminado los valores adecuados que conservan la potencia de la señal y el posicionamiento del canal de la forma más precisa posible. Para más información, consulte la introducción a la [asignación de canales predeterminada de XAudio2](xaudio2-default-channel-mapping.md) .

> [!Note]  
> XAudio2 ajusta automáticamente los niveles de volumen en función de la configuración de altavoz del usuario para mantener un nivel de volumen coherente en las configuraciones. Si la configuración del usuario no coincide con su configuración física, el volumen será demasiado alto o demasiado flexible en comparación con un sistema con una configuración precisa. Por ejemplo, un sistema configurado para altavoces de sonido envolvente 5,1 que solo tiene dos altavoces conectados suena demasiado blando. XAudio2 no puede detectar si la configuración de los altavoces de usuario coincide correctamente con la configuración física.

 

## <a name="pitch-control"></a>Control de paso

Los puntos se expresan como las proporciones de la tasa de entrada/salida entre 1/1024 y 1024/1, ambos inclusive. Una relación de 1/1024 reduce el tono en 10 octavas, mientras que una proporción de 1024/1 lo eleva en 10 octavos. Solo se puede usar el método [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar ajustes de tono a las voces de origen y solo si no se crearon con la \_ marca de voz \_ notono de XAUDIO2. La relación de frecuencia predeterminada es 1/1: es decir, ningún cambio de paso. En XAudio2. h se proporcionan dos funciones insertadas para realizar conversiones entre las relaciones de frecuencia y los semitonos: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) y [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de volumen y de paso](volume-and-pitch-control.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: cambiar el tono de la voz](how-to--change-voice-pitch.md)
</dt> <dt>

[Cómo: cambiar el volumen de la voz](how-to--change-voice-volume.md)
</dt> </dl>

 

 
