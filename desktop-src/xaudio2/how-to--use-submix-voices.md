---
description: En este tema se muestra cómo puede establecer grupos de voces para enviar su salida a la misma voz de submezcla. Esto permite que un solo cambio en una voz de submezcla afecte a todo un grupo de voces.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Cómo: usar voces de submezcla'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277596"
---
# <a name="how-to-use-submix-voices"></a>Cómo: usar voces de submezcla

En este tema se muestra cómo puede establecer grupos de voces para enviar su salida a la misma voz de submezcla. Esto permite que un solo cambio en una voz de submezcla afecte a todo un grupo de voces.

1.  Cree una [**voz de submezcla**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) a la que enviarán todas las voces de efecto sonoro del juego.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Creación de [**una \_ voz \_ de XAUDIO2 envía**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) una estructura que contiene una referencia a la voz de la submezcla.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Pass la [**voz de XAUDIO2 \_ \_ envía**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) la estructura a las nuevas voces de origen a medida que se crean.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Aplique los cambios a todas las voces de efecto sonoro ajustando la voz de la submezcla.

    En este ejemplo, el cambio del volumen de la voz de la submezcla con la función [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) cambia de forma eficaz el volumen de todas las voces que generan.

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

 

 
