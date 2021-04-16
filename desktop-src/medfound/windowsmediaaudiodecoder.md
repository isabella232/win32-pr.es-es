---
description: El descodificador de Windows Media Audio descodifica secuencias de audio codificadas por el codificador Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Descodificador de Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699409"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="d5976-103">Descodificador de Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="d5976-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="d5976-104">El descodificador de Windows Media Audio descodifica secuencias de audio codificadas por el [**codificador Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="d5976-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="d5976-105">El codificador y el descodificador admiten tres categorías de audio codificado: Windows Media Audio Standard, Windows Media Audio Professional y Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="d5976-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d5976-106">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="d5976-106">Class Identifier</span></span>

<span data-ttu-id="d5976-107">El identificador de clase (CLSID) del descodificador de Windows Media Audio se representa mediante la constante **\_ CWMADecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="d5976-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="d5976-108">Puede crear una instancia del descodificador de audio llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d5976-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="d5976-109">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5976-109">Input Formats</span></span>

<span data-ttu-id="d5976-110">En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de entrada admitidas por el descodificador de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="d5976-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="d5976-111">Para obtener información sobre cómo establecer los tipos de entrada y salida para el descodificador, consulte Configuración de la [descodificación de audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="d5976-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="d5976-112">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="d5976-112">Format tag constant</span></span>             | <span data-ttu-id="d5976-113">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d5976-113">Format tag value</span></span> | <span data-ttu-id="d5976-114">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="d5976-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="d5976-115">Formato de onda \_ \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="d5976-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="d5976-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="d5976-116">0x0161</span></span>           | <span data-ttu-id="d5976-117">Estándar Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="d5976-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="d5976-118">Formato de onda \_ \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="d5976-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="d5976-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="d5976-119">0x0162</span></span>           | <span data-ttu-id="d5976-120">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="d5976-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="d5976-121">formato de onda \_ \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="d5976-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="d5976-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="d5976-122">0x0163</span></span>           | <span data-ttu-id="d5976-123">Windows Media Audio sin pérdida de</span><span class="sxs-lookup"><span data-stu-id="d5976-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="d5976-124">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="d5976-124">Output Formats</span></span>

<span data-ttu-id="d5976-125">En la tabla siguiente se muestran las etiquetas de formato de audio que representan los tipos de salida admitidos por el **descodificador de Windows Media Audio**.</span><span class="sxs-lookup"><span data-stu-id="d5976-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="d5976-126">Para obtener información sobre cómo establecer los tipos de entrada y salida para el descodificador, consulte Configuración de la [codificación de audio](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="d5976-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="d5976-127">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="d5976-127">Format tag constant</span></span>       | <span data-ttu-id="d5976-128">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="d5976-128">Format tag value</span></span> | <span data-ttu-id="d5976-129">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="d5976-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="d5976-130">\_PCM con formato de onda \_</span><span class="sxs-lookup"><span data-stu-id="d5976-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="d5976-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="d5976-131">0x0001</span></span>           | <span data-ttu-id="d5976-132">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="d5976-132">PCM format</span></span>                                            |
| <span data-ttu-id="d5976-133">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="d5976-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="d5976-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="d5976-134">0x0003</span></span>           | <span data-ttu-id="d5976-135">Punto flotante IEEE</span><span class="sxs-lookup"><span data-stu-id="d5976-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="d5976-136">formato de onda \_ \_ extensible</span><span class="sxs-lookup"><span data-stu-id="d5976-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="d5976-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="d5976-137">0xFFFE</span></span>           | <span data-ttu-id="d5976-138">Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="d5976-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="d5976-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d5976-139">Interfaces</span></span>

<span data-ttu-id="d5976-140">Un objeto de descodificador de audio expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz **IMFTransform** para que el objeto pueda usarse como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d5976-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d5976-141">Un descodificador de Windows Media Audio se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d5976-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d5976-142">En la tabla siguiente se muestran las condiciones en las que un descodificador de audio se comporta como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="d5976-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d5976-143">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d5976-143">Operating system</span></span> | <span data-ttu-id="d5976-144">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="d5976-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5976-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d5976-145">Windows XP</span></span>       | <span data-ttu-id="d5976-146">Un descodificador de Windows Media Audio siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="d5976-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="d5976-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5976-147">Windows Vista</span></span>    | <span data-ttu-id="d5976-148">De forma predeterminada, un descodificador de Windows Media Audio se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="d5976-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="d5976-149">Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un descodificador de audio, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="d5976-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="d5976-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5976-150">Windows 7</span></span>        | <span data-ttu-id="d5976-151">De forma predeterminada, un descodificador de Windows Media Audio se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="d5976-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="d5976-152">Si obtiene una interfaz **IMFTransform** en un descodificador de audio, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="d5976-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="d5976-153">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d5976-153">Properties</span></span>

<span data-ttu-id="d5976-154">El descodificador de Windows Media Audio admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d5976-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5976-155">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d5976-155">Property</span></span></th>
<th><span data-ttu-id="d5976-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5976-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5976-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="d5976-158">Especifica el número máximo de muestras PCM adicionales que podrían devolverse al final de la descodificación de un archivo.</span><span class="sxs-lookup"><span data-stu-id="d5976-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="d5976-159">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="d5976-160">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="d5976-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-161">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d5976-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5976-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="d5976-163">Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.</span><span class="sxs-lookup"><span data-stu-id="d5976-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="d5976-164">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-164">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-165">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="d5976-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-166">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5976-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="d5976-168">Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="d5976-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="d5976-169">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-169">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-170">Profesional</span><span class="sxs-lookup"><span data-stu-id="d5976-170">Professional</span></span><br />
<span data-ttu-id="d5976-171">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5976-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="d5976-173">Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="d5976-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="d5976-174">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-174">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-175">Profesional, sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="d5976-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-176">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5976-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="d5976-178">Especifica si el descodificador de audio debe realizar Lt-Rt pliegue.</span><span class="sxs-lookup"><span data-stu-id="d5976-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="d5976-179">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="d5976-180">Professional.</span><span class="sxs-lookup"><span data-stu-id="d5976-180">Professional.</span></span><br />
<span data-ttu-id="d5976-181">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5976-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="d5976-183">Especifica la configuración de los altavoces en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="d5976-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="d5976-184">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-184">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-185">Professional.</span><span class="sxs-lookup"><span data-stu-id="d5976-185">Professional.</span></span><br />
<span data-ttu-id="d5976-186">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5976-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="d5976-188">Especifica el nivel de volumen medio del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="d5976-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="d5976-189">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-189">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-190">Profesional, sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="d5976-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-191">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d5976-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5976-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="d5976-193">Especifica el nivel de volumen medio deseado del contenido de audio de salida.</span><span class="sxs-lookup"><span data-stu-id="d5976-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="d5976-194">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-194">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-195">Profesional, sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="d5976-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-196">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5976-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="d5976-198">Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="d5976-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="d5976-199">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-199">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-200">Profesional, sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="d5976-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-201">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d5976-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5976-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5976-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="d5976-203">Especifica el nivel de volumen máximo deseado del contenido de audio de salida.</span><span class="sxs-lookup"><span data-stu-id="d5976-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="d5976-204">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5976-204">Windows XP and later.</span></span><br />
<span data-ttu-id="d5976-205">Profesional, sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="d5976-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="d5976-206">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d5976-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d5976-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5976-207">Requirements</span></span>



| <span data-ttu-id="d5976-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5976-208">Requirement</span></span> | <span data-ttu-id="d5976-209">Value</span><span class="sxs-lookup"><span data-stu-id="d5976-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5976-210">Remoto</span><span class="sxs-lookup"><span data-stu-id="d5976-210">Client</span></span><br/> | <span data-ttu-id="d5976-211">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5976-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="d5976-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5976-212">Header</span></span><br/> | <dl> <span data-ttu-id="d5976-213"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5976-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d5976-214">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5976-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="d5976-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5976-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5976-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5976-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5976-217">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="d5976-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d5976-218">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="d5976-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




