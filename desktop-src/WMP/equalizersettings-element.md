---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Aspectos de Windows Media Player, elemento EQUALIZERSETTINGS
- aspectos, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- referencia de las máscaras, elemento EQUALIZERSETTINGS
- elementos, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532164"
---
# <a name="equalizersettings-element"></a><span data-ttu-id="c69e2-108">Elemento EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="c69e2-108">EQUALIZERSETTINGS Element</span></span>

<span data-ttu-id="c69e2-109">El elemento **EQUALIZERSETTINGS** proporciona una manera de manipular el ecualizador gráfico y otras configuraciones de audio de Windows Media Player utilizando los atributos y el método que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="c69e2-109">The **EQUALIZERSETTINGS** element provides a way to manipulate the graphic equalizer and other audio settings of Windows Media Player using the attributes and method listed here.</span></span>

<span data-ttu-id="c69e2-110">El elemento **EQUALIZERSETTINGS** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="c69e2-110">The **EQUALIZERSETTINGS** element supports the following attributes.</span></span>



| <span data-ttu-id="c69e2-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="c69e2-111">Attribute</span></span>                                                          | <span data-ttu-id="c69e2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c69e2-112">Description</span></span>                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c69e2-113">bandas</span><span class="sxs-lookup"><span data-stu-id="c69e2-113">bands</span></span>](equalizersettings-bands.md)                               | <span data-ttu-id="c69e2-114">Recupera el número de bandas de frecuencia admitidas.</span><span class="sxs-lookup"><span data-stu-id="c69e2-114">Retrieves the number of frequency bands supported.</span></span>                                                      |
| [<span data-ttu-id="c69e2-115">alto</span><span class="sxs-lookup"><span data-stu-id="c69e2-115">bypass</span></span>](equalizersettings-bypass.md)                             | <span data-ttu-id="c69e2-116">Especifica o recupera un valor que indica si se omite el filtro del ecualizador en el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="c69e2-116">Specifies or retrieves a value indicating whether the equalizer filter is bypassed in the filter graph.</span></span> |
| [<span data-ttu-id="c69e2-117">Encadenada</span><span class="sxs-lookup"><span data-stu-id="c69e2-117">crossFade</span></span>](equalizersettings-crossfade.md)                       | <span data-ttu-id="c69e2-118">Especifica o recupera un valor que indica si está habilitado el fundido cruzado.</span><span class="sxs-lookup"><span data-stu-id="c69e2-118">Specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>                                |
| [<span data-ttu-id="c69e2-119">crossFadeWindow</span><span class="sxs-lookup"><span data-stu-id="c69e2-119">crossFadeWindow</span></span>](equalizersettings-crossfadewindow.md)           | <span data-ttu-id="c69e2-120">Especifica o recupera la cantidad de superposición entre fundidos en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c69e2-120">Specifies or retrieves the amount of cross-fade overlap in milliseconds.</span></span>                                |
| [<span data-ttu-id="c69e2-121">currentPreset</span><span class="sxs-lookup"><span data-stu-id="c69e2-121">currentPreset</span></span>](equalizersettings-currentpreset.md)               | <span data-ttu-id="c69e2-122">Especifica o recupera el índice del valor preestablecido actual.</span><span class="sxs-lookup"><span data-stu-id="c69e2-122">Specifies or retrieves the index of the current preset.</span></span>                                                 |
| [<span data-ttu-id="c69e2-123">currentPresetTitle</span><span class="sxs-lookup"><span data-stu-id="c69e2-123">currentPresetTitle</span></span>](equalizersettings-currentpresettitle.md)     | <span data-ttu-id="c69e2-124">Recupera el título del valor preestablecido actual.</span><span class="sxs-lookup"><span data-stu-id="c69e2-124">Retrieves the title of the current preset.</span></span>                                                              |
| [<span data-ttu-id="c69e2-125">currentSpeakerName</span><span class="sxs-lookup"><span data-stu-id="c69e2-125">currentSpeakerName</span></span>](equalizersettings-currentspeakername.md)     | <span data-ttu-id="c69e2-126">Recupera el nombre de la configuración del orador actual.</span><span class="sxs-lookup"><span data-stu-id="c69e2-126">Retrieves the name of the current speaker setting.</span></span>                                                      |
| [<span data-ttu-id="c69e2-127">enableSplineTension</span><span class="sxs-lookup"><span data-stu-id="c69e2-127">enableSplineTension</span></span>](equalizersettings-enablesplinetension.md)   | <span data-ttu-id="c69e2-128">Especifica o recupera un valor que indica si la tensión spline está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c69e2-128">Specifies or retrieves a value indicating whether spline tension is enabled or disabled.</span></span>                |
| [<span data-ttu-id="c69e2-129">enhancedAudio</span><span class="sxs-lookup"><span data-stu-id="c69e2-129">enhancedAudio</span></span>](equalizersettings-enhancedaudio.md)               | <span data-ttu-id="c69e2-130">Especifica o recupera un valor que indica si el audio mejorado está activado.</span><span class="sxs-lookup"><span data-stu-id="c69e2-130">Specifies or retrieves a value indicating whether enhanced audio is turned on.</span></span>                          |
| [<span data-ttu-id="c69e2-131">gainLevels</span><span class="sxs-lookup"><span data-stu-id="c69e2-131">gainLevels</span></span>](equalizersettings-gainlevels.md)                     | <span data-ttu-id="c69e2-132">Especifica o recupera el nivel de ganancia de la banda correspondiente al índice proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c69e2-132">Specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>                  |
| [<span data-ttu-id="c69e2-133">gainLevel1</span><span class="sxs-lookup"><span data-stu-id="c69e2-133">gainLevel1</span></span>](equalizersettings-gainlevel1.md)                     | <span data-ttu-id="c69e2-134">Especifica o recupera el nivel de ganancia de la banda 1.</span><span class="sxs-lookup"><span data-stu-id="c69e2-134">Specifies or retrieves the gain level of band 1.</span></span>                                                        |
| [<span data-ttu-id="c69e2-135">gainLevel2</span><span class="sxs-lookup"><span data-stu-id="c69e2-135">gainLevel2</span></span>](equalizersettings-gainlevel2.md)                     | <span data-ttu-id="c69e2-136">Especifica o recupera el nivel de ganancia de la banda 2.</span><span class="sxs-lookup"><span data-stu-id="c69e2-136">Specifies or retrieves the gain level of band 2.</span></span>                                                        |
| [<span data-ttu-id="c69e2-137">gainLevel3</span><span class="sxs-lookup"><span data-stu-id="c69e2-137">gainLevel3</span></span>](equalizersettings-gainlevel3.md)                     | <span data-ttu-id="c69e2-138">Especifica o recupera el nivel de ganancia de la banda 3.</span><span class="sxs-lookup"><span data-stu-id="c69e2-138">Specifies or retrieves the gain level of band 3.</span></span>                                                        |
| [<span data-ttu-id="c69e2-139">gainLevel4</span><span class="sxs-lookup"><span data-stu-id="c69e2-139">gainLevel4</span></span>](equalizersettings-gainlevel4.md)                     | <span data-ttu-id="c69e2-140">Especifica o recupera el nivel de ganancia de la banda 4.</span><span class="sxs-lookup"><span data-stu-id="c69e2-140">Specifies or retrieves the gain level of band 4.</span></span>                                                        |
| [<span data-ttu-id="c69e2-141">gainLevel5</span><span class="sxs-lookup"><span data-stu-id="c69e2-141">gainLevel5</span></span>](equalizersettings-gainlevel5.md)                     | <span data-ttu-id="c69e2-142">Especifica o recupera el nivel de ganancia de la banda 5.</span><span class="sxs-lookup"><span data-stu-id="c69e2-142">Specifies or retrieves the gain level of band 5.</span></span>                                                        |
| [<span data-ttu-id="c69e2-143">gainLevel6</span><span class="sxs-lookup"><span data-stu-id="c69e2-143">gainLevel6</span></span>](equalizersettings-gainlevel6.md)                     | <span data-ttu-id="c69e2-144">Especifica o recupera el nivel de ganancia de la banda 6.</span><span class="sxs-lookup"><span data-stu-id="c69e2-144">Specifies or retrieves the gain level of band 6.</span></span>                                                        |
| [<span data-ttu-id="c69e2-145">gainLevel7</span><span class="sxs-lookup"><span data-stu-id="c69e2-145">gainLevel7</span></span>](equalizersettings-gainlevel7.md)                     | <span data-ttu-id="c69e2-146">Especifica o recupera el nivel de ganancia de la banda 7.</span><span class="sxs-lookup"><span data-stu-id="c69e2-146">Specifies or retrieves the gain level of band 7.</span></span>                                                        |
| [<span data-ttu-id="c69e2-147">gainLevel8</span><span class="sxs-lookup"><span data-stu-id="c69e2-147">gainLevel8</span></span>](equalizersettings-gainlevel8.md)                     | <span data-ttu-id="c69e2-148">Especifica o recupera el nivel de ganancia de la banda 8.</span><span class="sxs-lookup"><span data-stu-id="c69e2-148">Specifies or retrieves the gain level of band 8.</span></span>                                                        |
| [<span data-ttu-id="c69e2-149">gainLevel9</span><span class="sxs-lookup"><span data-stu-id="c69e2-149">gainLevel9</span></span>](equalizersettings-gainlevel9.md)                     | <span data-ttu-id="c69e2-150">Especifica o recupera el nivel de ganancia de la banda 9.</span><span class="sxs-lookup"><span data-stu-id="c69e2-150">Specifies or retrieves the gain level of band 9.</span></span>                                                        |
| [<span data-ttu-id="c69e2-151">gainLevel10</span><span class="sxs-lookup"><span data-stu-id="c69e2-151">gainLevel10</span></span>](equalizersettings-gainlevel10.md)                   | <span data-ttu-id="c69e2-152">Especifica o recupera el nivel de ganancia de la banda 10.</span><span class="sxs-lookup"><span data-stu-id="c69e2-152">Specifies or retrieves the gain level of band 10.</span></span>                                                       |
| [<span data-ttu-id="c69e2-153">normalización</span><span class="sxs-lookup"><span data-stu-id="c69e2-153">normalization</span></span>](equalizersettings-normalization.md)               | <span data-ttu-id="c69e2-154">Especifica o recupera un valor que indica si está habilitada la normalización.</span><span class="sxs-lookup"><span data-stu-id="c69e2-154">Specifies or retrieves a value indicating whether normalization is enabled.</span></span>                             |
| [<span data-ttu-id="c69e2-155">normalizationAverage</span><span class="sxs-lookup"><span data-stu-id="c69e2-155">normalizationAverage</span></span>](equalizersettings-normalizationaverage.md) | <span data-ttu-id="c69e2-156">Recupera el valor de normalización promedio.</span><span class="sxs-lookup"><span data-stu-id="c69e2-156">Retrieves the average normalization value.</span></span>                                                              |
| [<span data-ttu-id="c69e2-157">normalizationPeak</span><span class="sxs-lookup"><span data-stu-id="c69e2-157">normalizationPeak</span></span>](equalizersettings-normalizationpeak.md)       | <span data-ttu-id="c69e2-158">Recupera el valor de normalización máximo.</span><span class="sxs-lookup"><span data-stu-id="c69e2-158">Retrieves the peak normalization value.</span></span>                                                                 |
| [<span data-ttu-id="c69e2-159">presetCount</span><span class="sxs-lookup"><span data-stu-id="c69e2-159">presetCount</span></span>](equalizersettings-presetcount.md)                   | <span data-ttu-id="c69e2-160">Recupera el número de valores preestablecidos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c69e2-160">Retrieves the number of presets available.</span></span>                                                              |
| [<span data-ttu-id="c69e2-161">Altavoces</span><span class="sxs-lookup"><span data-stu-id="c69e2-161">speakerSize</span></span>](equalizersettings-speakersize.md)                   | <span data-ttu-id="c69e2-162">Especifica o recupera el índice del tamaño de altavoz actual.</span><span class="sxs-lookup"><span data-stu-id="c69e2-162">Specifies or retrieves the index of the current speaker size.</span></span>                                           |
| [<span data-ttu-id="c69e2-163">splineTension</span><span class="sxs-lookup"><span data-stu-id="c69e2-163">splineTension</span></span>](equalizersettings-splinetension.md)               | <span data-ttu-id="c69e2-164">Especifica o recupera la tensión spline para el control de ecualizador.</span><span class="sxs-lookup"><span data-stu-id="c69e2-164">Specifies or retrieves the spline tension for the equalizer control.</span></span>                                    |
| [<span data-ttu-id="c69e2-165">truBassLevel</span><span class="sxs-lookup"><span data-stu-id="c69e2-165">truBassLevel</span></span>](equalizersettings-trubasslevel.md)                 | <span data-ttu-id="c69e2-166">Especifica o recupera el nivel de TruBass de SRS.</span><span class="sxs-lookup"><span data-stu-id="c69e2-166">Specifies or retrieves the SRS TruBass level.</span></span>                                                           |
| [<span data-ttu-id="c69e2-167">wowLevel</span><span class="sxs-lookup"><span data-stu-id="c69e2-167">wowLevel</span></span>](equalizersettings-wowlevel.md)                         | <span data-ttu-id="c69e2-168">Especifica o recupera el nivel de efecto SRS WOW.</span><span class="sxs-lookup"><span data-stu-id="c69e2-168">Specifies or retrieves the SRS WOW Effect level.</span></span>                                                        |



 

<span data-ttu-id="c69e2-169">El elemento **EQUALIZERSETTINGS** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="c69e2-169">The **EQUALIZERSETTINGS** element supports the following methods.</span></span>



| <span data-ttu-id="c69e2-170">Método</span><span class="sxs-lookup"><span data-stu-id="c69e2-170">Method</span></span>                                                 | <span data-ttu-id="c69e2-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="c69e2-171">Description</span></span>                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c69e2-172">nextPreset</span><span class="sxs-lookup"><span data-stu-id="c69e2-172">nextPreset</span></span>](equalizersettings-nextpreset.md)         | <span data-ttu-id="c69e2-173">Aplica el siguiente valor preestablecido del ecualizador.</span><span class="sxs-lookup"><span data-stu-id="c69e2-173">Applies the next equalizer preset.</span></span>                                   |
| [<span data-ttu-id="c69e2-174">presetTitle</span><span class="sxs-lookup"><span data-stu-id="c69e2-174">presetTitle</span></span>](equalizersettings-presettitle.md)       | <span data-ttu-id="c69e2-175">Recupera el nombre del valor preestablecido del ecualizador con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c69e2-175">Retrieves the name of the equalizer preset with the specified index.</span></span> |
| [<span data-ttu-id="c69e2-176">previousPreset</span><span class="sxs-lookup"><span data-stu-id="c69e2-176">previousPreset</span></span>](equalizersettings-previouspreset.md) | <span data-ttu-id="c69e2-177">Aplica el valor preestablecido del ecualizador anterior.</span><span class="sxs-lookup"><span data-stu-id="c69e2-177">Applies the previous equalizer preset.</span></span>                               |
| [<span data-ttu-id="c69e2-178">reset</span><span class="sxs-lookup"><span data-stu-id="c69e2-178">reset</span></span>](equalizersettings-reset.md)                   | <span data-ttu-id="c69e2-179">Restablece los niveles de ganancia de todas las bandas a cero decibelios.</span><span class="sxs-lookup"><span data-stu-id="c69e2-179">Resets the gain levels of all bands to zero decibels.</span></span>                |



 

<span data-ttu-id="c69e2-180">El elemento **EQUALIZERSETTINGS** puede implementar los controladores de eventos [ \_ onchange de atributo](attribute-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="c69e2-180">The **EQUALIZERSETTINGS** element can implement the [attribute\_onchange](attribute-onchange.md) event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c69e2-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c69e2-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c69e2-182">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="c69e2-182">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




