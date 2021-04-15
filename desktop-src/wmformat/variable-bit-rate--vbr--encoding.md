---
title: Codificación de velocidad de bits variable (VBR)
description: Codificación de velocidad de bits variable (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- SDK de Windows Media Format, codificación VBR
- Windows Media Format SDK, velocidad de bits variable (VBR)
- SDK de Windows Media Format, codificación VBR basada en la calidad
- SDK de Windows Media Format, codificación VBR sin restricciones
- SDK de Windows Media Format, codificación VBR restringida
- códecs, codificación VBR
- códecs, velocidad de bits variable (VBR)
- códecs, codificación VBR basada en la calidad
- códecs, codificación VBR sin restricciones
- códecs, codificación VBR restringida
- velocidad de bits variable (VBR), acerca de
- VBR (velocidad de bits variable), acerca de
- codificación VBR basada en la calidad, acerca de
- codificación VBR no restringida, acerca de
- codificación VBR restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714253"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="2444c-118">Codificación de velocidad de bits variable (VBR)</span><span class="sxs-lookup"><span data-stu-id="2444c-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="2444c-119">La codificación de velocidad de bits variable (VBR) es una alternativa a la codificación de velocidad de bits constante (CBR) y es compatible con algunos códecs.</span><span class="sxs-lookup"><span data-stu-id="2444c-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="2444c-120">Cuando la codificación CBR se esfuerza por mantener la velocidad de bits de los medios codificados, VBR se esfuerza por lograr la mejor calidad posible de los medios codificados.</span><span class="sxs-lookup"><span data-stu-id="2444c-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="2444c-121">La calidad del contenido codificado se determina por la cantidad de datos que se pierden al comprimir o descomprimir el contenido.</span><span class="sxs-lookup"><span data-stu-id="2444c-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="2444c-122">Hay varios factores que afectan a la pérdida de datos en el proceso de compresión, pero generalmente cuanto más complejos sean los datos originales y mayor sea la razón de compresión, más detalle se perderá en el proceso de compresión.</span><span class="sxs-lookup"><span data-stu-id="2444c-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="2444c-123">Hay tres tipos de codificación VBR: basado en la calidad, sin restricciones y restringidos.</span><span class="sxs-lookup"><span data-stu-id="2444c-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="2444c-124">Codificación VBR basada en la calidad</span><span class="sxs-lookup"><span data-stu-id="2444c-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="2444c-125">El primer tipo de codificación VBR está basado en la calidad, que usa un paso de codificación.</span><span class="sxs-lookup"><span data-stu-id="2444c-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="2444c-126">La codificación VBR basada en la calidad permite especificar un nivel de calidad para una secuencia de medios digitales en lugar de una velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="2444c-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="2444c-127">El códec codificará el contenido para que todos los ejemplos sean de calidad comparable.</span><span class="sxs-lookup"><span data-stu-id="2444c-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="2444c-128">La principal ventaja de la codificación VBR basada en la calidad es que la calidad es coherente dentro de un archivo y de un archivo al siguiente.</span><span class="sxs-lookup"><span data-stu-id="2444c-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="2444c-129">Por ejemplo, puede escribir un programa para copiar canciones de archivos de CD a ASF en un equipo.</span><span class="sxs-lookup"><span data-stu-id="2444c-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="2444c-130">En este caso, la calidad coherente es probablemente más importante para la experiencia del usuario final que el tamaño de archivo coherente.</span><span class="sxs-lookup"><span data-stu-id="2444c-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="2444c-131">El uso de la codificación VBR basada en la calidad garantiza que todas las canciones copiadas tengan la misma calidad.</span><span class="sxs-lookup"><span data-stu-id="2444c-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="2444c-132">La desventaja de la codificación VBR basada en la calidad es que no hay ninguna manera de conocer los requisitos de tamaño o ancho de banda de los medios codificados antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="2444c-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="2444c-133">Esto puede hacer que los archivos de codificación VBR basados en la calidad sean inadecuados para las circunstancias en las que la memoria o el ancho de banda están restringidos, como reproductores multimedia portátiles o conexiones a Internet de ancho de banda bajo.</span><span class="sxs-lookup"><span data-stu-id="2444c-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="2444c-134">En general, la codificación VBR basada en la calidad es idónea para la reproducción local o las conexiones de red de ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="2444c-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="2444c-135">En esos casos, la calidad coherente proporcionará una mejor experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="2444c-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="2444c-136">Codificación VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="2444c-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="2444c-137">La codificación VBR sin restricciones utiliza dos fases de codificación.</span><span class="sxs-lookup"><span data-stu-id="2444c-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="2444c-138">Cuando se usa la codificación VBR sin restricciones, se especifica una velocidad de bits para la secuencia, como lo haría con la codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="2444c-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="2444c-139">Sin embargo, el códec usa este valor solo como la velocidad de bits promedio para la secuencia y se codifica para que la calidad sea lo más alta posible mientras se mantiene el promedio.</span><span class="sxs-lookup"><span data-stu-id="2444c-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="2444c-140">La velocidad de bits real en cualquier punto de la secuencia codificada puede variar considerablemente respecto al valor medio.</span><span class="sxs-lookup"><span data-stu-id="2444c-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="2444c-141">No se establece una ventana de búfer para la codificación VBR sin restricciones como se haría con una secuencia con codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="2444c-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="2444c-142">En su lugar, el códec calcula el tamaño de la ventana de búfer necesaria en función de los requisitos de los ejemplos codificados.</span><span class="sxs-lookup"><span data-stu-id="2444c-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="2444c-143">La ventaja de la codificación VBR no restringida es que el flujo comprimido tiene la máxima calidad posible y permanece dentro de un ancho de banda medio predecible.</span><span class="sxs-lookup"><span data-stu-id="2444c-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="2444c-144">Codificación VBR restringida</span><span class="sxs-lookup"><span data-stu-id="2444c-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="2444c-145">La codificación VBR restringida es idéntica a la codificación VBR sin restricciones, salvo que se especifica una velocidad de bits máxima y una ventana de búfer máxima en el perfil.</span><span class="sxs-lookup"><span data-stu-id="2444c-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="2444c-146">A continuación, el códec usa los valores máximos para determinar cómo comprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="2444c-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="2444c-147">Si establece los valores máximos lo suficientemente altos, la codificación VBR restringida producirá la misma secuencia codificada que la codificación VBR sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="2444c-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2444c-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2444c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2444c-149">**Elección de un método de codificación**</span><span class="sxs-lookup"><span data-stu-id="2444c-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="2444c-150">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="2444c-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2444c-151">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="2444c-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="2444c-152">**Configuración de secuencias VBR**</span><span class="sxs-lookup"><span data-stu-id="2444c-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="2444c-153">**Codificación de velocidad de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="2444c-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="2444c-154">**Codificación de dos pasos**</span><span class="sxs-lookup"><span data-stu-id="2444c-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="2444c-155">**Uso de la codificación de Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="2444c-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




