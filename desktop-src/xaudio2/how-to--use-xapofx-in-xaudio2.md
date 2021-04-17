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
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="e8d42-103">Cómo: usar XAPOFX en XAudio2</span><span class="sxs-lookup"><span data-stu-id="e8d42-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="e8d42-104">En este tema se muestra cómo usar uno de los efectos incluidos en XAPOFX en una cadena de efectos de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e8d42-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="e8d42-105">Para usar un efecto de XAPOFX en una cadena de efectos de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e8d42-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="e8d42-106">Cree el efecto pasando el CLSID de un efecto XAPOFX a la función [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .</span><span class="sxs-lookup"><span data-stu-id="e8d42-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="e8d42-107">En este caso, se crea el efecto de reverberación simplificado FXReverb.</span><span class="sxs-lookup"><span data-stu-id="e8d42-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="e8d42-108">Rellenar una estructura de [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.</span><span class="sxs-lookup"><span data-stu-id="e8d42-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="e8d42-109">Rellenar una estructura de [**\_ \_ cadena de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.</span><span class="sxs-lookup"><span data-stu-id="e8d42-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="e8d42-110">Aplique la cadena de efectos a una voz de XAudio2 con la función [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="e8d42-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="e8d42-111">También puede aplicar una cadena de efectos a una voz cuando cree la voz pasando la cadena como un parámetro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="e8d42-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="e8d42-112">Libere el efecto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="e8d42-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="e8d42-113">Al crear un XAPO, tendrá un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="e8d42-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="e8d42-114">Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa el recuento de referencias en el XAPO.</span><span class="sxs-lookup"><span data-stu-id="e8d42-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="e8d42-115">La liberación de la referencia del cliente a XAPO permite a XAudio2 tomar posesión del XAPO.</span><span class="sxs-lookup"><span data-stu-id="e8d42-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="e8d42-116">Si XAudio2 tiene la única referencia a XAPO, esta referencia se elimina cuando se deja de usar en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e8d42-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="e8d42-117">Si el código de cliente necesita mantener una referencia a XAPO (por ejemplo, para reutilizarlo más adelante), puede omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="e8d42-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="e8d42-118">Rellena la estructura del parámetro, si existe, asociada al efecto.</span><span class="sxs-lookup"><span data-stu-id="e8d42-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="e8d42-119">En este caso, la estructura de [**\_ parámetros FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) se usa para establecer la difusión y el tamaño de la sala que el efecto de reverberación debe usar.</span><span class="sxs-lookup"><span data-stu-id="e8d42-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="e8d42-120">Para pasar la estructura del parámetro de efecto al efecto, llame a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.</span><span class="sxs-lookup"><span data-stu-id="e8d42-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e8d42-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8d42-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8d42-122">Efectos de audio</span><span class="sxs-lookup"><span data-stu-id="e8d42-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="e8d42-123">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e8d42-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
