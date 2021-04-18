---
description: 'Hay tres tipos de objetos de voz de XAudio2: voces de origen, submezcla y maestra.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voces de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707123"
---
# <a name="xaudio2-voices"></a>Voces de XAudio2

Hay tres tipos de objetos de voz de XAudio2: voces de *origen*, *submezcla* y *maestra* . Las voces de origen operan en datos de audio proporcionados por el cliente. Las voces de origen y de submezcla envían su resultado a una o más voces de submezcla o de procesamiento. Las voces de submezcla y de procesamiento mezclan el audio de todas las voces que les alimentan y trabajan con el resultado. Las voces de procesamiento escriben datos de audio en un dispositivo de audio.

## <a name="actions-performed-by-all-voices"></a>Acciones realizadas por todas las voces

Todas las voces realizan las siguientes acciones por orden en el audio que viaja.

1.  Ajuste general del volumen, que afecta a todos los canales de audio. Vea [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Cadena opcional especificada por el cliente de uno o más efectos de DSP, como la reverberación integrada o un efecto de usuario definido por la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) . Consulte [efectos de audio de XAudio2](xaudio2-audio-effects.md).
3.  Ajuste del volumen de salida por canal. Vea [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Combinación de matriz independiente en cada una de las voces de destino o en el dispositivo de salida de audio para la maestra de voces. Esta mezcla cambia el número de canales en el audio, si es necesario.

## <a name="source-voices"></a>Voces de origen

Use las voces de origen para enviar datos de audio a la canalización de procesamiento de XAudio2. Son los puntos de entrada en el [gráfico de audio de XAudio2](xaudio2-audio-graph.md). Debe enviar datos de voz a una voz de patrón para que se escuche, ya sea directamente o a través de voces de submezcla intermedias.

Además de las acciones realizadas por todas las voces, las voces de origen realizan las siguientes acciones.

-   Si es necesario, un descodificador se ejecuta primero para convertir los datos de origen codificados en modulación por pulsos de código (PCM).
-   Una conversión de frecuencia de muestreo de velocidad variable (SRC) convierte los datos de audio de origen de la voz a la velocidad de muestra esperada por las voces de destino, si es necesario, y también admite cambios de paso dinámicos.
-   Se puede usar un filtro opcional de variable de estado para colorear el sonido de varias maneras. Vea [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Se puede aplicar un filtro opcional a las salidas de la voz. Vea [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Voces de submezcla

Una voz de submezcla se usa principalmente para mejorar el rendimiento y el procesamiento de efectos. No se pueden enviar búferes de datos directamente a voces de submezcla. No será audible a menos que lo envíe a una voz de maestro. Puede utilizar una voz de submezcla para asegurarse de que un conjunto determinado de datos de voz se convierte en el mismo formato y de que una cadena de efectos determinada se procese en el resultado colectivo.

Además de las acciones realizadas por todas las voces, las voces de submezcla realizan las siguientes acciones.

-   Un SRC de velocidad fija se ejecuta en la salida de la voz, si es necesario, para convertir el audio a la velocidad de muestra esperada por sus voces de destino.
-   Se puede usar un filtro opcional de variable de estado para colorear el sonido de varias maneras. Vea [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Se puede aplicar un filtro opcional a las salidas de la voz. Vea [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Voces de mastering

Use una voz de maestro para representar el dispositivo de salida de audio. Los búferes de datos no se pueden enviar directamente a las voces de la maestra, pero los datos enviados a otros tipos de voces deben dirigirse a una voz de patrón para que se escuche.

Además de las acciones realizadas por todas las voces, las voces de Master realizan las siguientes acciones.

-   Si crea la voz de masterización con un valor de *InputSampleRate* explícito que no es compatible con el dispositivo de audio, se usa un src de velocidad fija para realizar la conversión a la velocidad de muestra más cercana admitida por el dispositivo.
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

 

 
