---
description: 'Hay tres tipos de objetos de voz XAudio2: voces de origen, submezcla y mastering.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voces de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b756033be5b64dbf03e3b3756902014774a53c9aebc8f41a1df1f982685cca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025943"
---
# <a name="xaudio2-voices"></a>Voces de XAudio2

Hay tres tipos de objetos de voz XAudio2: *de* origen, *de submezcla* y *de* maestro. Las voces de origen operan en datos de audio proporcionados por el cliente. Las voces de origen y de submezcla envían su resultado a una o más voces de submezcla o de procesamiento. Las voces de submezcla y de procesamiento mezclan el audio de todas las voces que les alimentan y trabajan con el resultado. Las voces de procesamiento escriben datos de audio en un dispositivo de audio.

## <a name="actions-performed-by-all-voices"></a>Acciones realizadas por todas las voces

Todas las voces realizan las siguientes acciones en orden en el audio que viaja a través de ellas.

1.  Ajuste general del volumen, que afecta a todos los canales de audio. Vea [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Cadena opcional especificada por el cliente de uno o varios efectos de DSP, como la reverberación integrada o un efecto de usuario definido por la [**interfaz IXAPO.**](/windows/desktop/api/XAPO/nn-xapo-ixapo) Vea [Efectos de audio de XAudio2.](xaudio2-audio-effects.md)
3.  Ajuste del volumen de salida por canal. Vea [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Separe la combinación de matrices con cada una de las voces de destino o con el dispositivo de salida de audio para dominar las voces. Esta combinación cambia el número de canales del audio, si es necesario.

## <a name="source-voices"></a>Voces de origen

Use voces de origen para enviar datos de audio a la canalización de procesamiento de XAudio2. Son los puntos de entrada en el audio [de XAudio2 Graph](xaudio2-audio-graph.md). Debe enviar datos de voz a una voz maestra para que se escuche, ya sea directamente o a través de voces de submezcla intermedias.

Además de las acciones realizadas por todas las voces, las voces de origen realizan las siguientes acciones.

-   Si es necesario, un descodificador se ejecuta en primer lugar para convertir los datos de origen codificados en Pulse Code Decoder (PCM).
-   Una conversión de frecuencia de muestreo de velocidad variable (SRC) convierte los datos de audio de origen de la voz a la velocidad de muestreo esperada por sus voces de destino, si es necesario, y también admite cambios dinámicos de tono.
-   Se puede usar un filtro de variable de estado opcional para colorear el sonido de varias maneras. Vea [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Se puede aplicar un filtro opcional a las salidas de la voz. Vea [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Submezclar voces

Una voz de submezcla se usa principalmente para mejorar el rendimiento y procesar los efectos. No se pueden enviar búferes de datos directamente a las voces de submezcla. No será sondible a menos que la envíe a una voz maestra. Puede usar una submezcla de voz para asegurarse de que un conjunto determinado de datos de voz se convierte al mismo formato y para que se procese una cadena de efecto determinada en el resultado colectivo.

Además de las acciones realizadas por todas las voces, las voces de submezcla realizan las siguientes acciones.

-   Un SRC de velocidad fija se ejecuta en la salida de la voz, si es necesario, para convertir el audio a la frecuencia de muestreo esperada por sus voces de destino.
-   Se puede usar un filtro de variable de estado opcional para colorear el sonido de varias maneras. Vea [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Se puede aplicar un filtro opcional a las salidas de la voz. Vea [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Mastering Voices

Use una voz maestra para representar el dispositivo de salida de audio. No se pueden enviar búferes de datos directamente a voces maestras, pero los datos enviados a otros tipos de voces deben ir a una voz maestra para que se escuche.

Además de las acciones realizadas por todas las voces, las voces maestras realizan las siguientes acciones.

-   Si crea la voz maestra con un valor *InputSampleRate* explícito que no es compatible con el dispositivo de audio, se usa un SRC de velocidad fija para convertir a la frecuencia de muestreo más cercana compatible con el dispositivo.
-   Recorte el audio de salida final, si lo requiere el dispositivo de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
