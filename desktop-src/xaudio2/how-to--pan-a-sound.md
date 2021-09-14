---
description: En este tema se muestra cómo puede establecer la matriz de salida de una voz de origen mono que se genera en una voz maestra estéreo con el fin de lograr el movimiento panorámico entre los altavoces izquierdo y derecho.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Cómo: Desplazar un sonido'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255945"
---
# <a name="how-to-pan-a-sound"></a>Cómo: Desplazar un sonido

En este tema se muestra cómo puede establecer la matriz de salida de una voz de origen mono que se genera en una voz maestra estéreo con el fin de lograr el movimiento panorámico entre los altavoces izquierdo y derecho.

## <a name="to-setup-panning"></a>Para configurar el movimiento panorámico

1.  Recupere la configuración del hablante [**mediante IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Cree una matriz para contener la matriz de salida. El tamaño mínimo de la matriz de salida es el número de canales de la voz de origen multiplicado por el número de canales de la voz de salida. En este caso, una matriz de ocho elementos controlará una salida de voz mono en cualquier formato de salida de hasta 7.1 sonido envolvente.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Calcule los niveles de envío en función del movimiento panorámico deseado entre los altavoces izquierdo y derecho. En este ejemplo, los valores de panorámica oscilarán entre -1 y 1 con -1 que indica todo el sonido en el altavoz izquierdo y 1 indica todo el sonido al altavoz derecho.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Establezca los índices de matriz de salida correspondientes a los altavoces izquierdo y derecho con los valores calculados en el paso anterior. Los altavoces izquierdo y derecho se determinan al mirar la máscara de canal devuelta por [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask). Puesto que los canales siempre se deben codificar en el orden especificado en la página de referencia [**DESUSOTEXTENSIBLE,**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) es posible determinar el índice de matriz correspondiente a un hablante individual.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Aplique la matriz de salida a la voz de origen [**mediante IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix). La voz de origen será una voz de origen o una voz de submezcla que se envía a una voz de submezcla o a una voz maestra. Puede obtener información sobre las voces de origen y destino, como su número de canales, mediante [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Control de volumen y tono de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
