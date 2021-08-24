---
description: En este tema se muestra cómo puede aplicar una cadena de efectos a una voz para permitir el procesamiento personalizado de los datos de audio para esa voz. En este tema se describe cómo usar el efecto de reverberación, que es uno de los efectos XAudio2 integrados.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Cómo: crear un efecto en cadena'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abd6372fe07f71d75a4963f6617cdeda15ecf8390e3142fcf110029bd8f6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838417"
---
# <a name="how-to-create-an-effect-chain"></a>Cómo: crear un efecto en cadena

En este tema se muestra cómo puede aplicar una cadena de efectos a una voz para permitir el procesamiento personalizado de los datos de audio para esa voz. En este tema se describe cómo usar el efecto de reverberación, que es uno de los efectos XAudio2 integrados.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>Para crear una cadena de efectos básica que aplique un efecto a una voz

1.  Cree el efecto.

    En este ejemplo, la [**función XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crea un efecto de reverberación. Consulte [Efectos de audio de XAudio2](xaudio2-audio-effects.md) para obtener una lista de posibles orígenes de efectos para su uso con XAudio2.

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Rellene una [**estructura DEL DESCRIPTOR DE EFECTO \_ \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.

    Si hay varios efectos en la cadena, cada efecto necesitará una estructura [**DESCRIPTOR DE \_ EFECTO \_ XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Rellene una [**estructura EFFECT \_ \_ CHAIN de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos. En este caso, la cadena solo tiene un efecto. Si la cadena tiene más de un efecto, el miembro EffectCount contendrá el recuento de efectos y el miembro pEffectDescriptors apuntará a una matriz de estructuras DESCRIPTOR DE EFECTO \_ \_ XAUDIO2.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Aplique la cadena de efectos a una voz con la [**función SetEffectChain.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)

    Puede aplicar cadenas de efecto a voces maestras, voces de origen y voces de submezcla.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Libere el efecto con IUnknown::Release.

    Al crear un XAPO, tendrá un recuento de referencias de 1. Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)XAudio2 incrementa el recuento de referencias en el XAPO. Liberar la referencia del cliente a XAPO permite que XAudio2 tome posesión del XAPO. Si XAudio2 tiene la única referencia al XAPO, se desechará cuando XAudio2 ya no lo esté utilizando. Si el código de cliente necesita mantener una referencia a XAPO (por ejemplo, para su reutilización posterior), debe omitir este paso.

    ```
    pXAPO->Release();
    ```

    

6.  Rellene la estructura de parámetros, si la hubiera, asociada al efecto. El efecto reverberación usa una [**estructura \_ PARAMETERS de REVERB \_ de XAUDIO2FX.**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  Pase la estructura de parámetros de efecto al efecto mediante una llamada a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Deshabilite o habilite el efecto, siempre que corresponda.

    Puede usar [**DisableEffect en cualquier**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) momento para desactivar un efecto.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Puede volver a activar un efecto con [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).

    ```
    pVoice->EnableEffect(0);
    ```

    

    Los parámetros de [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) [**y EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) especifican el efecto en la cadena que se va a habilitar o deshabilitar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Información general sobre XAPO](xapo-overview.md)
</dt> <dt>

[Cómo: Usar XAOPFX en XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Cómo: Usar un XAOP en XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
