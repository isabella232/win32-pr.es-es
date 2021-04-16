---
description: 'El codificador Windows Media Audio codifica secuencias de audio. El codificador admite tres categorías de salida codificada: Windows Media Audio estándar, Windows Media Audio Professional y Windows Media Audio sin pérdida de información.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificador Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718940"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="b92c8-104">Codificador Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="b92c8-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="b92c8-105">El codificador Windows Media Audio codifica secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="b92c8-106">El codificador admite tres categorías de salida codificada: Windows Media Audio estándar, Windows Media Audio Professional y Windows Media Audio sin pérdida de información.</span><span class="sxs-lookup"><span data-stu-id="b92c8-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b92c8-107">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="b92c8-107">Class Identifier</span></span>

<span data-ttu-id="b92c8-108">El identificador de clase (CLSID) del codificador Windows Media Audio se representa mediante la constante CWMAEncMediaObject de **CLSID \_**.</span><span class="sxs-lookup"><span data-stu-id="b92c8-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="b92c8-109">Puede crear una instancia del codificador de audio llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b92c8-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="b92c8-110">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="b92c8-110">Input Formats</span></span>

<span data-ttu-id="b92c8-111">En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de entrada admitidas por el codificador de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="b92c8-112">Para obtener información sobre cómo establecer los tipos de entrada y salida para el codificador, consulte [configuración](configuringaudioencoding.md)de la codificación de audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="b92c8-113">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="b92c8-113">Format tag constant</span></span>       | <span data-ttu-id="b92c8-114">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="b92c8-114">Format tag value</span></span> | <span data-ttu-id="b92c8-115">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="b92c8-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="b92c8-116">\_PCM con formato de onda \_</span><span class="sxs-lookup"><span data-stu-id="b92c8-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="b92c8-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="b92c8-117">0x0001</span></span>           | <span data-ttu-id="b92c8-118">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="b92c8-118">PCM format</span></span>                                            |
| <span data-ttu-id="b92c8-119">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="b92c8-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="b92c8-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="b92c8-120">0x0003</span></span>           | <span data-ttu-id="b92c8-121">Punto flotante IEEE</span><span class="sxs-lookup"><span data-stu-id="b92c8-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="b92c8-122">formato de onda \_ \_ extensible</span><span class="sxs-lookup"><span data-stu-id="b92c8-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="b92c8-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="b92c8-123">0xFFFE</span></span>           | <span data-ttu-id="b92c8-124">Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="b92c8-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="b92c8-125">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="b92c8-125">Output Formats</span></span>

<span data-ttu-id="b92c8-126">En la tabla siguiente se muestran las etiquetas de formato de audio que representan las categorías de salida admitidas por el codificador de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="b92c8-127">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="b92c8-127">Format tag constant</span></span>             | <span data-ttu-id="b92c8-128">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="b92c8-128">Format tag value</span></span> | <span data-ttu-id="b92c8-129">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="b92c8-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="b92c8-130">Formato de onda \_ \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="b92c8-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="b92c8-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="b92c8-131">0x0161</span></span>           | <span data-ttu-id="b92c8-132">Estándar Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="b92c8-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="b92c8-133">Formato de onda \_ \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="b92c8-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="b92c8-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="b92c8-134">0x0162</span></span>           | <span data-ttu-id="b92c8-135">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="b92c8-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="b92c8-136">formato de onda \_ \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="b92c8-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="b92c8-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="b92c8-137">0x0163</span></span>           | <span data-ttu-id="b92c8-138">Windows Media Audio sin pérdida de</span><span class="sxs-lookup"><span data-stu-id="b92c8-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="b92c8-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b92c8-139">Interfaces</span></span>

<span data-ttu-id="b92c8-140">Un objeto endoder de audio expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="b92c8-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="b92c8-141">Un codificador de Windows Media Audio se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b92c8-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="b92c8-142">En la tabla siguiente se muestran las condiciones en las que un codificador de audio se comporta como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="b92c8-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="b92c8-143">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b92c8-143">Operating system</span></span> | <span data-ttu-id="b92c8-144">Comportamiento del codificador</span><span class="sxs-lookup"><span data-stu-id="b92c8-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92c8-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b92c8-145">Windows XP</span></span>       | <span data-ttu-id="b92c8-146">Un codificador Windows Media Audio siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="b92c8-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="b92c8-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b92c8-147">Windows Vista</span></span>    | <span data-ttu-id="b92c8-148">De forma predeterminada, un codificador de Windows Media Audio se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="b92c8-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="b92c8-149">Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un codificador de audio, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="b92c8-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="b92c8-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b92c8-150">Windows 7</span></span>        | <span data-ttu-id="b92c8-151">De forma predeterminada, un codificador de Windows Media Audio se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="b92c8-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="b92c8-152">Si obtiene una interfaz **IMFTransform** en un codificador de audio, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="b92c8-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="b92c8-153">Propiedades del codificador</span><span class="sxs-lookup"><span data-stu-id="b92c8-153">Encoder Properties</span></span>

<span data-ttu-id="b92c8-154">El codificador Windows Media Audio admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b92c8-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b92c8-155">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b92c8-155">Property</span></span></th>
<th><span data-ttu-id="b92c8-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="b92c8-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b92c8-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-158">Especifica si el codificador utiliza la codificación VBR de promedio controlable.</span><span class="sxs-lookup"><span data-stu-id="b92c8-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="b92c8-159">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-160">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-161">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-163">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en su velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="b92c8-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="b92c8-164">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-164">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-165">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-165">Standard, Professional.</span></span><br />
<span data-ttu-id="b92c8-166">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-168">Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="b92c8-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="b92c8-169">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-170">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-171">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-173">Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.</span><span class="sxs-lookup"><span data-stu-id="b92c8-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="b92c8-174">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-175">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-176">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-178">Especifica si la complejidad del algoritmo de codificación está restringida.</span><span class="sxs-lookup"><span data-stu-id="b92c8-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="b92c8-179">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-180">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-181">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-183">Especifica si el codificador está restringido por un requisito de latencia máximo.</span><span class="sxs-lookup"><span data-stu-id="b92c8-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="b92c8-184">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-185">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-186">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-188">Especifica si los modos enumerados por el codificador están limitados a aquellos que cumplen un requisito de calidad.</span><span class="sxs-lookup"><span data-stu-id="b92c8-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="b92c8-189">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-190">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-191">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-193">Especifica el perfil de complejidad del contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="b92c8-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="b92c8-194">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-194">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-195">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-196">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-198">Especifica el nivel de calidad deseado para la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="b92c8-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="b92c8-199">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-200">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-201">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-203">Especifica si el codificador utiliza la sustitución de ruido.</span><span class="sxs-lookup"><span data-stu-id="b92c8-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="b92c8-204">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-205">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-206">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-208">Especifica si el codificador utiliza la limitación de intervalo PCM.</span><span class="sxs-lookup"><span data-stu-id="b92c8-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="b92c8-209">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-210">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-211">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-213">Especifica el ancho de banda máximo codificado permitido por el truncamiento de banda en el codificador.</span><span class="sxs-lookup"><span data-stu-id="b92c8-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="b92c8-214">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-215">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-216">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-218">Especifica el ancho de banda mínimo codificado permitido por el truncamiento de banda en el codificador.</span><span class="sxs-lookup"><span data-stu-id="b92c8-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="b92c8-219">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-220">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-221">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-223">Especifica la calidad con la que se permite el ancho de banda mínimo codificado.</span><span class="sxs-lookup"><span data-stu-id="b92c8-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="b92c8-224">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-225">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-226">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-228">Especifica la calidad con la que se permite el ancho de banda máximo codificado.</span><span class="sxs-lookup"><span data-stu-id="b92c8-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="b92c8-229">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-230">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-231">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-233">Especifica si el codificador realiza el truncamiento de la banda.</span><span class="sxs-lookup"><span data-stu-id="b92c8-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="b92c8-234">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-235">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-236">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-238">Especifica si el codificador usa el estilo de cálculo de máscara realizado por la versión 7 del codificador Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="b92c8-239">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-240">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-241">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-243">Especifica si el codificador realiza el procesamiento de imágenes estéreo.</span><span class="sxs-lookup"><span data-stu-id="b92c8-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="b92c8-244">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-245">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-246">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-248">Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de media controlable.</span><span class="sxs-lookup"><span data-stu-id="b92c8-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="b92c8-249">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-250">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-251">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-253">Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="b92c8-254">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-255">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-256">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-258">Especifica la complejidad del algoritmo de codificación.</span><span class="sxs-lookup"><span data-stu-id="b92c8-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="b92c8-259">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-260">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-261">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-263">Especifica el final de una fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="b92c8-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="b92c8-264">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-264">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-265">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-265">Standard, Professional.</span></span><br />
<span data-ttu-id="b92c8-266">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-268">Especifica si el codificador básico usa la &quot; característica Plus &quot; .</span><span class="sxs-lookup"><span data-stu-id="b92c8-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="b92c8-269">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-270">Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-270">Professional.</span></span><br />
<span data-ttu-id="b92c8-271">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-273">Especifica la latencia máxima del descodificador, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b92c8-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="b92c8-274">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-275">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-276">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-278">Especifica la latencia máxima del codificador, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b92c8-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="b92c8-279">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-280">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-281">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-283">Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="b92c8-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="b92c8-284">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-285">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-286">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-288">Especifica el número máximo de pasos admitidos por el codificador.</span><span class="sxs-lookup"><span data-stu-id="b92c8-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="b92c8-289">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-289">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-290">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-291">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-293">Especifica el número de pasos que usará el codificador para codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="b92c8-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="b92c8-294">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-294">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-295">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-296">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-298">Especifica si el codificador está restringido por una velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="b92c8-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="b92c8-299">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-300">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-300">Standard, Professional.</span></span><br />
<span data-ttu-id="b92c8-301">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-303">Especifica el número preferido de muestras por fotograma.</span><span class="sxs-lookup"><span data-stu-id="b92c8-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="b92c8-304">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-305">Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-305">Professional.</span></span><br />
<span data-ttu-id="b92c8-306">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-308">Especifica si el codificador debe usar un tamaño de marco preferido.</span><span class="sxs-lookup"><span data-stu-id="b92c8-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="b92c8-309">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-310">Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-310">Professional.</span></span><br />
<span data-ttu-id="b92c8-311">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-313">Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la codificación de velocidad de bits variable (VBR) de dos pasos restringidos.</span><span class="sxs-lookup"><span data-stu-id="b92c8-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="b92c8-314">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-314">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-315">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-315">Standard, Professional.</span></span><br />
<span data-ttu-id="b92c8-316">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-318">Especifica la ventana de búfer promedio, en milisegundos, de una secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="b92c8-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="b92c8-319">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-319">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-320">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-321">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-323">Especifica la ventana de búfer máxima, en milisegundos, de una secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="b92c8-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="b92c8-324">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-324">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-325">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-326">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-328">Especifica la velocidad de bits media, en bits por segundo, de una secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="b92c8-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="b92c8-329">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-329">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-330">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-331">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-333">Especifica la velocidad de bits máxima, en bits por segundo, de una secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="b92c8-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="b92c8-334">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-334">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-335">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-336">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-338">Especifica si el codificador utiliza la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="b92c8-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="b92c8-339">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-339">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-340">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-341">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-343">Esta propiedad no se usa actualmente en el códec de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-345">Especifica el nivel de volumen medio del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="b92c8-346">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-346">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-347">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-348">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-350">Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="b92c8-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="b92c8-351">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-351">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-352">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-353">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-355">Especifica el promedio de bytes por segundo para el audio codificado VBR.</span><span class="sxs-lookup"><span data-stu-id="b92c8-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="b92c8-356">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-356">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-357">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-358">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b92c8-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-360">Especifica si el codificador debe producir 1 paquete WMA por fotograma.</span><span class="sxs-lookup"><span data-stu-id="b92c8-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="b92c8-361">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-362">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-363">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-365">Especifica si el codificador debe generar parámetros de control de intervalo dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b92c8-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="b92c8-366">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-367">Standard, Professional y Lossless.</span><span class="sxs-lookup"><span data-stu-id="b92c8-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b92c8-368">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b92c8-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-370">Especifica la estructura <strong>WAVEFORMATEX</strong> que describe el contenido de audio de entrada.</span><span class="sxs-lookup"><span data-stu-id="b92c8-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="b92c8-371">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-371">Windows XP and later.</span></span><br />
<span data-ttu-id="b92c8-372">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-372">Standard, Professional.</span></span><br />
<span data-ttu-id="b92c8-373">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b92c8-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="b92c8-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="b92c8-375">Especifica si el codificador debe habilitar la codificación S/PDIF en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="b92c8-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="b92c8-376">Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b92c8-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="b92c8-377">Professional.</span><span class="sxs-lookup"><span data-stu-id="b92c8-377">Professional.</span></span><br />
<span data-ttu-id="b92c8-378">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92c8-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b92c8-379">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92c8-379">Requirements</span></span>



| <span data-ttu-id="b92c8-380">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92c8-380">Requirement</span></span> | <span data-ttu-id="b92c8-381">Value</span><span class="sxs-lookup"><span data-stu-id="b92c8-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b92c8-382">Remoto</span><span class="sxs-lookup"><span data-stu-id="b92c8-382">Client</span></span><br/> | <span data-ttu-id="b92c8-383">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="b92c8-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="b92c8-384">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b92c8-384">Header</span></span><br/> | <dl> <span data-ttu-id="b92c8-385"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b92c8-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b92c8-386">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b92c8-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="b92c8-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b92c8-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b92c8-388">Vea también</span><span class="sxs-lookup"><span data-stu-id="b92c8-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92c8-389">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="b92c8-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="b92c8-390">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="b92c8-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




