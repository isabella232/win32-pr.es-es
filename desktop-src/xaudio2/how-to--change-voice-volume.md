---
description: En este tema se muestra cómo puede cambiar el volumen de una voz en un nivel general, en cada canal de salida o entre cada canal de una voz y otra voz en su lista de envío.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Cómo: Cambiar volumen de voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab433cc0e5c0e3ddc4bea3c58f49afae36cf8833fa8f003c99f1c45b237c70a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696263"
---
# <a name="how-to-change-voice-volume"></a>Cómo: Cambiar volumen de voz

En este tema se muestra cómo puede cambiar el volumen de una voz en un nivel general, en cada canal de salida o entre cada canal de una voz y otra voz en su [**lista de envío.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>Para establecer un nivel de volumen general para la entrada de voz

-   Use la [**función SetVolume.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>Para establecer el volumen de los canales de salida de la voz

1.  Cree una matriz de números de punto flotante que contenga los volúmenes deseados de todos los canales de salida de la voz.

    La matriz tendrá una entrada para cada canal de la voz.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Use la [**función SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) para establecer el volumen de los canales de salida.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>Para establecer el volumen de conexiones

Establezca el volumen de conexión entre la voz y una voz en su [**lista de envío.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)

1.  Cree una matriz de números de punto flotante que defina una matriz de salida si la voz se envía a otra voz.

    > [!Note]  
    > La matriz debe tener un número de entradas igual a los canales de voz de origen × canales de voz de destino. En este ejemplo, la asignación es de una voz con un canal a una voz con dos canales.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Use la [**función SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para establecer la matriz de salida.

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Control de volumen y tono de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
