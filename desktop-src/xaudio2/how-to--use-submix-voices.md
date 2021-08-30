---
description: En este tema se muestra cómo puede establecer grupos de voces para enviar su salida a la misma voz de submezcla. Esto permite que un único cambio en una voz de submezcla afecte a todo un grupo de voces.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Cómo: usar voces de submezcla'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688a190bcf105945c3b596960083d850955d2b9f59bb6a991dfb6d120bd7b713
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005825"
---
# <a name="how-to-use-submix-voices"></a>Cómo: usar voces de submezcla

En este tema se muestra cómo puede establecer grupos de voces para enviar su salida a la misma voz de submezcla. Esto permite que un único cambio en una voz de submezcla afecte a todo un grupo de voces.

1.  Cree una [**voz de submezcla**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) a la que se enviarán todas las voces de efecto de sonido del juego.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Cree una [**estructura XAUDIO2 \_ VOICE \_ SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) que contenga una referencia a la voz de submezcla.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Pase la [**estructura XAUDIO2 \_ VOICE \_ SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) a nuevas voces de origen a medida que se crean.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Aplique cambios a todas las voces de efecto de sonido ajustando la voz de submezcla.

    En este ejemplo, cambiar el volumen de la submezcla de voz con la función [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) cambia de forma eficaz el volumen de todas las voces que se le emiten.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
