---
description: En este tema se muestra cómo puede elevar o reducir el tono de los datos de audio cambiando su velocidad de reproducción mediante la función SetFrequencyRatio en una voz de origen.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Cómo: Cambiar el tono de voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926475"
---
# <a name="how-to-change-voice-pitch"></a>Cómo: Cambiar el tono de voz

En este tema se muestra cómo puede elevar o reducir el tono de los datos de audio cambiando su velocidad de reproducción mediante la función [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) en una voz de origen.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Para cambiar el tono de una voz de origen

1.  Determine la relación de frecuencia deseada para la [**voz de origen.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Consulte Control de volumen y tono de [XAudio2](xaudio2-volume-and-pitch-control.md) para obtener más información sobre cómo calcular la relación de frecuencia.

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Use la [**función SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para establecer la relación de frecuencia de la voz de origen.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Control de volumen y tono de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
