---
title: Plantillas de cumplimiento de dispositivos de audio
description: Plantillas de cumplimiento de dispositivos de audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos
- SDK de Windows Media Format, plantillas de conformidad de dispositivos de audio
- Advanced Systems Format (ASF), plantillas de conformidad de dispositivos de audio
- ASF (formato de sistemas avanzados), plantillas de conformidad de dispositivos de audio
- Códec de Windows Media Audio 9, plantillas de conformidad de dispositivos de audio
- códecs, códec de Windows Media Audio 9
- plantillas de conformidad de dispositivos, vídeo
- plantillas de cumplimiento de dispositivos de audio
- plantillas, plantillas de conformidad de dispositivos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357077"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="cf428-114">Plantillas de cumplimiento de dispositivos de audio</span><span class="sxs-lookup"><span data-stu-id="cf428-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="cf428-115">En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Audio 9, o posterior.</span><span class="sxs-lookup"><span data-stu-id="cf428-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="cf428-116">Cadena de plantilla</span><span class="sxs-lookup"><span data-stu-id="cf428-116">Template string</span></span> | <span data-ttu-id="cf428-117">Intervalo de velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="cf428-117">Bit rate range</span></span>     | <span data-ttu-id="cf428-118">Notas</span><span class="sxs-lookup"><span data-stu-id="cf428-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf428-119">Nivel</span><span class="sxs-lookup"><span data-stu-id="cf428-119">"L1"</span></span>            | <span data-ttu-id="cf428-120">64 Kbps 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="cf428-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="cf428-121">Esta plantilla está pensada para dispositivos solo de audio restringidos.</span><span class="sxs-lookup"><span data-stu-id="cf428-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="cf428-122">L2</span><span class="sxs-lookup"><span data-stu-id="cf428-122">"L2"</span></span>            | <span data-ttu-id="cf428-123"><= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="cf428-123"><= 160 Kbps</span></span>     | <span data-ttu-id="cf428-124">Esta plantilla corresponde a la clase 4 del kit de portabilidad de Windows Media Audio, que admite toda la implementación del descodificador de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="cf428-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="cf428-125">Caché</span><span class="sxs-lookup"><span data-stu-id="cf428-125">"L3"</span></span>            | <span data-ttu-id="cf428-126"><= 384 Kbps</span><span class="sxs-lookup"><span data-stu-id="cf428-126"><= 384 Kbps</span></span>     | <span data-ttu-id="cf428-127">Esta plantilla corresponde a la clase 4 del kit de portabilidad de Windows Media Audio, que admite toda la implementación del descodificador de Windows Media Audio. El intervalo de velocidad de bits es la única diferencia entre esta plantilla y L2.</span><span class="sxs-lookup"><span data-stu-id="cf428-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="cf428-128">CG</span><span class="sxs-lookup"><span data-stu-id="cf428-128">"L"</span></span>             | <span data-ttu-id="cf428-129">Velocidades de bits</span><span class="sxs-lookup"><span data-stu-id="cf428-129">All bit rates</span></span>      | <span data-ttu-id="cf428-130">Esta plantilla solo se usa con equipos personales y se utiliza normalmente para mostrar todas las capacidades del códec.</span><span class="sxs-lookup"><span data-stu-id="cf428-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="cf428-131">En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec de voz de Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="cf428-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="cf428-132">Cadena de plantilla</span><span class="sxs-lookup"><span data-stu-id="cf428-132">Template string</span></span> | <span data-ttu-id="cf428-133">Intervalo de velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="cf428-133">Bit rate range</span></span> | <span data-ttu-id="cf428-134">Notas</span><span class="sxs-lookup"><span data-stu-id="cf428-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf428-135">S1</span><span class="sxs-lookup"><span data-stu-id="cf428-135">"S1"</span></span>            | <span data-ttu-id="cf428-136"><= 20 Kbps</span><span class="sxs-lookup"><span data-stu-id="cf428-136"><= 20 Kbps</span></span>  | <span data-ttu-id="cf428-137">Esta plantilla está pensada solo para dispositivos de poca complejidad. Esta plantilla es solo voz.</span><span class="sxs-lookup"><span data-stu-id="cf428-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="cf428-138">S2</span><span class="sxs-lookup"><span data-stu-id="cf428-138">"S2"</span></span>            | <span data-ttu-id="cf428-139"><= 20 Kbps</span><span class="sxs-lookup"><span data-stu-id="cf428-139"><= 20 Kbps</span></span>  | <span data-ttu-id="cf428-140">Esta es la plantilla recomendada para la mayoría de las aplicaciones. Esta plantilla admite combinaciones de voz y música.</span><span class="sxs-lookup"><span data-stu-id="cf428-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="cf428-141">En la tabla siguiente se enumeran las plantillas de conformidad del dispositivo y los parámetros asociados para el códec Windows Media Audio 9 Professional o posterior.</span><span class="sxs-lookup"><span data-stu-id="cf428-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="cf428-142">Cadena de plantilla</span><span class="sxs-lookup"><span data-stu-id="cf428-142">Template string</span></span> | <span data-ttu-id="cf428-143">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf428-143">Properties</span></span>                                                                                   | <span data-ttu-id="cf428-144">Notas</span><span class="sxs-lookup"><span data-stu-id="cf428-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf428-145">Conector</span><span class="sxs-lookup"><span data-stu-id="cf428-145">"M1"</span></span>            | <span data-ttu-id="cf428-146">Velocidad de bits <= 384 tasa de KbpsSampling <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="cf428-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="cf428-147">Canales <= 5,1</span><span class="sxs-lookup"><span data-stu-id="cf428-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="cf428-148">Esta plantilla se recomienda para películas estándar con sonido envolvente.</span><span class="sxs-lookup"><span data-stu-id="cf428-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="cf428-149">²</span><span class="sxs-lookup"><span data-stu-id="cf428-149">"M2"</span></span>            | <span data-ttu-id="cf428-150">Velocidad de bits <= 768 tasa de KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="cf428-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="cf428-151">Canales <= 5,1</span><span class="sxs-lookup"><span data-stu-id="cf428-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="cf428-152">Esta plantilla se recomienda para películas de alta definición con sonido envolvente.</span><span class="sxs-lookup"><span data-stu-id="cf428-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="cf428-153">M3</span><span class="sxs-lookup"><span data-stu-id="cf428-153">"M3"</span></span>            | <span data-ttu-id="cf428-154">Velocidad de bits <= 1.500 tasa de KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="cf428-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="cf428-155">Canales <= 7,1</span><span class="sxs-lookup"><span data-stu-id="cf428-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="cf428-156">Esta plantilla se recomienda para películas de alta definición con sonido envolvente de 8 canales, como contenido codificado para presentación en teatro.</span><span class="sxs-lookup"><span data-stu-id="cf428-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="cf428-157">"M"</span><span class="sxs-lookup"><span data-stu-id="cf428-157">"M"</span></span>             | <span data-ttu-id="cf428-158">Tasas de muestreo de todos los bits ratesAll</span><span class="sxs-lookup"><span data-stu-id="cf428-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="cf428-159">Todos los canales</span><span class="sxs-lookup"><span data-stu-id="cf428-159">All channels</span></span><br/>                           | <span data-ttu-id="cf428-160">Esta plantilla solo se usa con equipos personales y se utiliza normalmente para mostrar todas las capacidades del códec. Esta es también la designación de plantilla para todo el audio codificado con el códec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="cf428-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cf428-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf428-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf428-162">**Parámetros de plantilla de conformidad de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="cf428-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="cf428-163">**Combinaciones recomendadas de plantillas de cumplimiento de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="cf428-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="cf428-164">**Plantillas de cumplimiento de dispositivos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="cf428-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





