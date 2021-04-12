---
title: Acerca del complemento DSP de audio de ejemplo
description: Acerca del complemento DSP de audio de ejemplo
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Complementos de Media Player de Windows, ejemplos
- complementos, ejemplos
- Complementos de procesamiento de señal digital, ejemplos
- Complementos DSP, ejemplos
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, ejemplos de audio
- Complementos DSP, ejemplos de audio
- ejemplos, Complementos DSP
- Complementos de DSP de audio, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357131"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="da53a-113">Acerca del complemento DSP de audio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="da53a-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="da53a-114">El complemento DSP de audio de ejemplo proporciona una implementación de procesamiento simple que escala la amplitud del audio mediante un factor proporcionado por el usuario en la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="da53a-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="da53a-115">El complemento acepta valores entre cero y 1.</span><span class="sxs-lookup"><span data-stu-id="da53a-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="da53a-116">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="da53a-116">The default value is 1.</span></span> <span data-ttu-id="da53a-117">Un valor de 1 no tiene ningún efecto sobre el sonido; otros factores de escala son multiplicadores de los ejemplos de audio.</span><span class="sxs-lookup"><span data-stu-id="da53a-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="da53a-118">Por ejemplo, un valor de 0,5 daría como resultado una disminución de 6 decibelios en el volumen.</span><span class="sxs-lookup"><span data-stu-id="da53a-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="da53a-119">Un valor de cero da como resultado un silencio.</span><span class="sxs-lookup"><span data-stu-id="da53a-119">A value of zero results in silence.</span></span>

<span data-ttu-id="da53a-120">El complemento DSP de audio de ejemplo funciona con audio PCM estéreo o mono.</span><span class="sxs-lookup"><span data-stu-id="da53a-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da53a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da53a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da53a-122">**Crear un complemento DSP**</span><span class="sxs-lookup"><span data-stu-id="da53a-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




