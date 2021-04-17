---
description: En este tema se muestra cómo usar uno de los efectos incluidos en XAPOFX en una cadena de efectos de XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Cómo: usar XAPOFX en XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696590"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Cómo: usar XAPOFX en XAudio2

En este tema se muestra cómo usar uno de los efectos incluidos en XAPOFX en una cadena de efectos de XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Para usar un efecto de XAPOFX en una cadena de efectos de XAudio2

1.  Cree el efecto pasando el CLSID de un efecto XAPOFX a la función [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .

    En este caso, se crea el efecto de reverberación simplificado FXReverb.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Rellenar una estructura de [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Rellenar una estructura de [**\_ \_ cadena de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Aplique la cadena de efectos a una voz de XAudio2 con la función [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > También puede aplicar una cadena de efectos a una voz cuando cree la voz pasando la cadena como un parámetro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Libere el efecto con IUnknown:: Release. Al crear un XAPO, tendrá un recuento de referencias de 1. Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa el recuento de referencias en el XAPO. La liberación de la referencia del cliente a XAPO permite a XAudio2 tomar posesión del XAPO. Si XAudio2 tiene la única referencia a XAPO, esta referencia se elimina cuando se deja de usar en XAudio2. Si el código de cliente necesita mantener una referencia a XAPO (por ejemplo, para reutilizarlo más adelante), puede omitir este paso.

    ```
    pXAPO->Release();
    ```

    

6.  Rellena la estructura del parámetro, si existe, asociada al efecto.

    En este caso, la estructura de [**\_ parámetros FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) se usa para establecer la difusión y el tamaño de la sala que el efecto de reverberación debe usar.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Para pasar la estructura del parámetro de efecto al efecto, llame a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 
