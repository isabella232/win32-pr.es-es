---
description: En este tema se muestra cómo puede aumentar o reducir el paso de los datos de audio cambiando la velocidad de reproducción mediante la función SetFrequencyRatio en una voz de origen.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Cómo: cambiar el tono de la voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154617"
---
# <a name="how-to-change-voice-pitch"></a>Cómo: cambiar el tono de la voz

En este tema se muestra cómo puede aumentar o reducir el paso de los datos de audio cambiando la velocidad de reproducción mediante la función [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) en una voz de origen.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Para cambiar el tono de una voz de origen

1.  Determine la relación de frecuencia deseada para la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Consulte [volumen de XAudio2 y control de paso](xaudio2-volume-and-pitch-control.md) para obtener más información sobre cómo calcular la relación de frecuencia.

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Utilice la función [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para establecer la relación de frecuencia de la voz de origen.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Volumen y control de paso de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
