---
description: En este tema se muestra cómo usar un efecto creado con la API de XAPO en una cadena de efectos de XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Cómo: usar un XAPO en XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686968"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>Cómo: usar un XAPO en XAudio2

En este tema se muestra cómo usar un efecto creado con la API de XAPO en una cadena de efectos de XAudio2.

1.  Cree el XAPO tal y como se describe en [Cómo: crear un xapo](how-to--create-an-xapo.md).

    También puede implementar la funcionalidad de parámetros en tiempo de ejecución tal y como se describe en [Cómo: agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

2.  Cree una instancia de XAPO.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Rellenar una estructura de [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Rellenar una estructura de [**\_ \_ cadena de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Aplique la cadena de efectos a una voz de XAudio2 con la función [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Una cadena de efectos también se puede aplicar a una voz cuando se crea la voz pasando la cadena como un parámetro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

6.  Libere el efecto con IUnknown:: Release.

    Al crear un XAPO, tendrá un recuento de referencias de 1. Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa el recuento de referencias en el XAPO. La liberación de la referencia del cliente a XAPO permite a XAudio2 tomar posesión del XAPO. Si XAudio2 tiene la única referencia a XAPO, se desechará cuando XAudio2 ya no la use en XAudio2. Si el código de cliente necesita mantener una referencia a XAPO para su reutilización posterior, por ejemplo, debe omitir este paso.

    ```
    pXAPO->Release();
    ```

    

7.  Rellena la estructura del parámetro, si existe, asociada al efecto. En este caso, el porcentaje de intensidad total a la que se debe aplicar el efecto.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Para pasar la estructura del parámetro de efecto al efecto, llame a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Información general de XAPO](xapo-overview.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 
