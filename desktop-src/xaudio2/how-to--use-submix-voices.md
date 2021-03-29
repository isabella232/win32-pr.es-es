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
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="87da6-104">Cómo: usar voces de submezcla</span><span class="sxs-lookup"><span data-stu-id="87da6-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="87da6-105">En este tema se muestra cómo puede establecer grupos de voces para enviar su salida a la misma voz de submezcla.</span><span class="sxs-lookup"><span data-stu-id="87da6-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="87da6-106">Esto permite que un solo cambio en una voz de submezcla afecte a todo un grupo de voces.</span><span class="sxs-lookup"><span data-stu-id="87da6-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="87da6-107">Cree una [**voz de submezcla**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) a la que enviarán todas las voces de efecto sonoro del juego.</span><span class="sxs-lookup"><span data-stu-id="87da6-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="87da6-108">Creación de [**una \_ voz \_ de XAUDIO2 envía**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) una estructura que contiene una referencia a la voz de la submezcla.</span><span class="sxs-lookup"><span data-stu-id="87da6-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="87da6-109">Pass la [**voz de XAUDIO2 \_ \_ envía**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) la estructura a las nuevas voces de origen a medida que se crean.</span><span class="sxs-lookup"><span data-stu-id="87da6-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="87da6-110">Aplique los cambios a todas las voces de efecto sonoro ajustando la voz de la submezcla.</span><span class="sxs-lookup"><span data-stu-id="87da6-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="87da6-111">En este ejemplo, el cambio del volumen de la voz de la submezcla con la función [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) cambia de forma eficaz el volumen de todas las voces que generan.</span><span class="sxs-lookup"><span data-stu-id="87da6-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="87da6-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87da6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87da6-113">Voces</span><span class="sxs-lookup"><span data-stu-id="87da6-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="87da6-114">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="87da6-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="87da6-115">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="87da6-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
