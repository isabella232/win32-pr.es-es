---
description: En este tema se muestra cómo usar uno de los efectos incluidos en XAPOFX en una cadena de efectos XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Cómo: usar XAPOFX en XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618e508d5e023c29c373193aa38da9d0e7f9f76c94a57f63e50df0c346426b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696156"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Cómo: usar XAPOFX en XAudio2

En este tema se muestra cómo usar uno de los efectos incluidos en XAPOFX en una cadena de efectos XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Para usar un efecto de XAPOFX en una cadena de efectos XAudio2

1.  Cree el efecto pasando el CLSID de un efecto XAPOFX a la [**función CreateFX.**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)

    En este caso, se crea el efecto de reverberación simplificado FXReverb.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Rellene una [**estructura DEL DESCRIPTOR DE EFECTO \_ \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Rellene una [**estructura \_ EFFECT \_ CHAIN de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Aplique la cadena de efectos a una voz XAudio2 con la [**función SetEffectChain.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > También puede aplicar una cadena de efectos a una voz al crear la voz pasando la cadena como parámetro a [**IXAudio2::CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Libere el efecto con IUnknown::Release. Al crear un XAPO, tendrá un recuento de referencias de 1. Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)XAudio2 incrementa el recuento de referencias en el XAPO. Liberar la referencia del cliente a XAPO permite que XAudio2 tome posesión del XAPO. Si XAudio2 tiene la única referencia al XAPO, esta referencia se elimina cuando XAudio2 ya no la usa. Si el código de cliente necesita mantener una referencia al XAPO (por ejemplo, para reutilizarlo más adelante), puede omitir este paso.

    ```
    pXAPO->Release();
    ```

    

6.  Rellene la estructura de parámetros, si la hay, asociada al efecto.

    En este caso, la estructura PARAMETERS de [**FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) se usa para establecer el tamaño de habitación y la reverberación que debe usar el efecto de reverberación.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Pase la estructura del parámetro de efecto al efecto mediante una llamada a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 
