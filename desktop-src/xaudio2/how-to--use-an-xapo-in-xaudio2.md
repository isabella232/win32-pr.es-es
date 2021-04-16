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
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="c7b3e-103">Cómo: usar un XAPO en XAudio2</span><span class="sxs-lookup"><span data-stu-id="c7b3e-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="c7b3e-104">En este tema se muestra cómo usar un efecto creado con la API de XAPO en una cadena de efectos de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="c7b3e-105">Cree el XAPO tal y como se describe en [Cómo: crear un xapo](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="c7b3e-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="c7b3e-106">También puede implementar la funcionalidad de parámetros en tiempo de ejecución tal y como se describe en [Cómo: agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="c7b3e-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="c7b3e-107">Cree una instancia de XAPO.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="c7b3e-108">Rellenar una estructura de [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con datos.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="c7b3e-109">Rellenar una estructura de [**\_ \_ cadena de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con datos.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="c7b3e-110">Aplique la cadena de efectos a una voz de XAudio2 con la función [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="c7b3e-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="c7b3e-111">Una cadena de efectos también se puede aplicar a una voz cuando se crea la voz pasando la cadena como un parámetro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="c7b3e-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="c7b3e-112">Libere el efecto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="c7b3e-113">Al crear un XAPO, tendrá un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="c7b3e-114">Cuando el XAPO se pasa a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa el recuento de referencias en el XAPO.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="c7b3e-115">La liberación de la referencia del cliente a XAPO permite a XAudio2 tomar posesión del XAPO.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="c7b3e-116">Si XAudio2 tiene la única referencia a XAPO, se desechará cuando XAudio2 ya no la use en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="c7b3e-117">Si el código de cliente necesita mantener una referencia a XAPO para su reutilización posterior, por ejemplo, debe omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="c7b3e-118">Rellena la estructura del parámetro, si existe, asociada al efecto.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="c7b3e-119">En este caso, el porcentaje de intensidad total a la que se debe aplicar el efecto.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="c7b3e-120">Para pasar la estructura del parámetro de efecto al efecto, llame a la función [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) en la voz a la que está asociado el efecto.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c7b3e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7b3e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b3e-122">Efectos de audio</span><span class="sxs-lookup"><span data-stu-id="c7b3e-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="c7b3e-123">Información general de XAPO</span><span class="sxs-lookup"><span data-stu-id="c7b3e-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="c7b3e-124">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="c7b3e-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
