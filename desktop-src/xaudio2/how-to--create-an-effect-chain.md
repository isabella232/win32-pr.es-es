---
description: En este tema se muestra cómo puede aplicar una cadena de efectos a una voz para permitir el procesamiento personalizado de los datos de audio de esa voz. En este tema se describe cómo usar el efecto Reverberación, que es uno de los efectos de XAudio2 integrados.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Cómo: crear un efecto en cadena'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154616"
---
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="46b46-104">Cómo: crear un efecto en cadena</span><span class="sxs-lookup"><span data-stu-id="46b46-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="46b46-105">En este tema se muestra cómo puede aplicar una cadena de efectos a una voz para permitir el procesamiento personalizado de los datos de audio de esa voz.</span><span class="sxs-lookup"><span data-stu-id="46b46-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="46b46-106">En este tema se describe cómo usar el efecto Reverberación, que es uno de los efectos de XAudio2 integrados.</span><span class="sxs-lookup"><span data-stu-id="46b46-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="46b46-107">Para crear una cadena de efectos básicos que aplique un efecto a una voz</span><span class="sxs-lookup"><span data-stu-id="46b46-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="46b46-108">Cree el efecto.</span><span class="sxs-lookup"><span data-stu-id="46b46-108">Create the effect.</span></span>

    <span data-ttu-id="46b46-109">En este ejemplo, la función [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crea un efecto de reverberación.</span><span class="sxs-lookup"><span data-stu-id="46b46-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="46b46-110">Consulte [efectos de audio de XAudio2](xaudio2-audio-effects.md) para obtener una lista de posibles orígenes de efectos para su uso con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46b46-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="46b46-111">Rellenar una estructura de [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.</span><span class="sxs-lookup"><span data-stu-id="46b46-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="46b46-112">Si hay varios efectos en la cadena, cada efecto necesitará una estructura [**de \_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="46b46-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="46b46-113">Rellenar una estructura de [**\_ \_ cadena de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.</span><span class="sxs-lookup"><span data-stu-id="46b46-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="46b46-114">En este caso, la cadena solo tiene un efecto.</span><span class="sxs-lookup"><span data-stu-id="46b46-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="46b46-115">Si la cadena tiene más de un efecto, el miembro EffectCount contendrá el recuento de efectos y el miembro pEffectDescriptors apuntará a una matriz de \_ estructuras de \_ descriptor de efectos de XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="46b46-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="46b46-116">Aplique la cadena de efectos a una voz con la función [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="46b46-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="46b46-117">Puede aplicar cadenas de efectos a las voces maestras, las voces de origen y las voces de submezcla.</span><span class="sxs-lookup"><span data-stu-id="46b46-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="46b46-118">Libere el efecto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="46b46-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="46b46-119">Al crear un XAPO, tendrá un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="46b46-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="46b46-120">Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa el recuento de referencias en el XAPO.</span><span class="sxs-lookup"><span data-stu-id="46b46-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="46b46-121">La liberación de la referencia del cliente a XAPO permite a XAudio2 tomar posesión del XAPO.</span><span class="sxs-lookup"><span data-stu-id="46b46-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="46b46-122">Si XAudio2 tiene la única referencia a XAPO, se desechará cuando XAudio2 ya no la use en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46b46-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="46b46-123">Si el código de cliente necesita mantener una referencia a XAPO (por ejemplo, para reutilizarlo más adelante), debe omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="46b46-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="46b46-124">Rellena la estructura del parámetro, si existe, asociada al efecto.</span><span class="sxs-lookup"><span data-stu-id="46b46-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="46b46-125">El efecto de reverberación utiliza una estructura de [**\_ \_ parámetros de reverberación XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .</span><span class="sxs-lookup"><span data-stu-id="46b46-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

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

    

7.  <span data-ttu-id="46b46-126">Para pasar la estructura del parámetro de efecto al efecto, llame a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.</span><span class="sxs-lookup"><span data-stu-id="46b46-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="46b46-127">Deshabilitar o habilitar el efecto, siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="46b46-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="46b46-128">Puede usar [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) en cualquier momento para desactivar un efecto.</span><span class="sxs-lookup"><span data-stu-id="46b46-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="46b46-129">Puede volver a activar un efecto con [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span><span class="sxs-lookup"><span data-stu-id="46b46-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="46b46-130">Los parámetros de [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) y [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) especifican el efecto de la cadena que se va a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="46b46-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46b46-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46b46-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46b46-132">Efectos de audio</span><span class="sxs-lookup"><span data-stu-id="46b46-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="46b46-133">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="46b46-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="46b46-134">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="46b46-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="46b46-135">Información general de XAPO</span><span class="sxs-lookup"><span data-stu-id="46b46-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="46b46-136">Cómo: usar XAOPFX en XAudio2</span><span class="sxs-lookup"><span data-stu-id="46b46-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="46b46-137">Cómo: usar un XAOP en XAudio2</span><span class="sxs-lookup"><span data-stu-id="46b46-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
