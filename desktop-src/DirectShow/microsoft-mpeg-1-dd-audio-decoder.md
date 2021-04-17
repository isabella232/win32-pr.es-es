---
description: 'Este filtro descodifica los formatos de audio siguientes:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Descodificador de audio MPEG-1/DD/AAC de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686343"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="6c472-103">Descodificador de audio MPEG-1/DD/AAC de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c472-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="6c472-104">Este filtro descodifica los formatos de audio siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c472-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="6c472-105">Capas de audio I y II de MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="6c472-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="6c472-106">Audio MPEG-2 compatible con versiones anteriores, las capas I y II (ISO/IEC 13818-3), mono y estéreo solamente.</span><span class="sxs-lookup"><span data-stu-id="6c472-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="6c472-107">Perfil de baja complejidad (LC) de codificación de audio avanzado (AAC).</span><span class="sxs-lookup"><span data-stu-id="6c472-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="6c472-108">High-Efficiency AAC (HE-AAC) versión 1 y versión 2.</span><span class="sxs-lookup"><span data-stu-id="6c472-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="6c472-109">Sistemas de cine digital de paso a través (DTS) para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="6c472-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="6c472-110">LPCM, mono y estéreo únicamente, con o sin encabezados de PES.</span><span class="sxs-lookup"><span data-stu-id="6c472-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="6c472-111">Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="6c472-111">Dolby Digital.</span></span>
-   <span data-ttu-id="6c472-112">Dolby Digital Plus, incluida la conversión de Dolby Digital Plus a Dolby digital para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="6c472-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="6c472-113">La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c472-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c472-114">Este filtro no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="6c472-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="6c472-115">La descodificación de los formatos Dolby Digital Plus, AAC y HE-AAC requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6c472-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="6c472-116">No se admite la descodificación de Dolby digital o Dolby Digital Plus en Windows 7 Home Basic o Windows 7 Starter.</span><span class="sxs-lookup"><span data-stu-id="6c472-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="6c472-117">En el registro, el nombre descriptivo de este filtro es "Microsoft DTV-DVD audio descodificador".</span><span class="sxs-lookup"><span data-stu-id="6c472-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="6c472-118">Información de filtro</span><span class="sxs-lookup"><span data-stu-id="6c472-118">Filter Information</span></span>

<span data-ttu-id="6c472-119">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="6c472-119">Filter Interfaces</span></span>

[<span data-ttu-id="6c472-120">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6c472-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="6c472-121">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6c472-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="6c472-122">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="6c472-122">Input Pin Media Types</span></span>

<span data-ttu-id="6c472-123">En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="6c472-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="6c472-124">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-125">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="6c472-126">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="6c472-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="6c472-127">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-128">**MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-129">**MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ DTS** (véase la nota 2).</span><span class="sxs-lookup"><span data-stu-id="6c472-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="6c472-130">**MEDIATYPE \_ \_ \_ paquete de DVD cifrado**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-131">**MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-132">**MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-133">**MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (véase la nota 2).</span><span class="sxs-lookup"><span data-stu-id="6c472-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="6c472-134">**MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-135">**MEDIATYPE \_ MPEG2 \_ PES**, **\_ \_ audio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="6c472-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-136">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-137">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="6c472-138">**MEDIATYPE \_ Streaming**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="6c472-139">A partir de Windows 7, el filtro también admite los siguientes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="6c472-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="6c472-140">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-141">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DTS2** (véase la nota 2).</span><span class="sxs-lookup"><span data-stu-id="6c472-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="6c472-142">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ de \_ \_ audio LPCM de DVD**</span><span class="sxs-lookup"><span data-stu-id="6c472-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="6c472-143">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVM** (véase la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-144">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="6c472-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="6c472-145">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ loa**</span><span class="sxs-lookup"><span data-stu-id="6c472-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="6c472-146">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="6c472-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="6c472-147">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ raw \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="6c472-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="6c472-148">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vea la nota 1).</span><span class="sxs-lookup"><span data-stu-id="6c472-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="6c472-149">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="6c472-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="6c472-150">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ loa**</span><span class="sxs-lookup"><span data-stu-id="6c472-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="6c472-151">El tipo de entrada puede cambiar dinámicamente durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="6c472-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="6c472-152">Para obtener más información acerca de estos tipos de medios, consulte [**subtipos de audio**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="6c472-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="6c472-153">La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c472-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="6c472-154">Para la entrada de sistemas de cine digital (DTS), solo se admite la salida S/PDIF (DTS sobre S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="6c472-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="6c472-155">No se admite la descodificación de audio.</span><span class="sxs-lookup"><span data-stu-id="6c472-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="6c472-156">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="6c472-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="6c472-157">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6c472-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="6c472-158">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="6c472-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="6c472-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="6c472-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="6c472-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6c472-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6c472-161">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6c472-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="6c472-162">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="6c472-162">Output Pin Media Types</span></span>

<span data-ttu-id="6c472-163">En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de salida:</span><span class="sxs-lookup"><span data-stu-id="6c472-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="6c472-164">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (igual que **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital**)</span><span class="sxs-lookup"><span data-stu-id="6c472-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="6c472-165">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="6c472-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="6c472-166">A partir de Windows 7, el filtro también admite los siguientes tipos de salida:</span><span class="sxs-lookup"><span data-stu-id="6c472-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="6c472-167">**MEDIATYPE \_ Audio**, **\_ subtipo de KSDATAFORMAT \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="6c472-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="6c472-168">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="6c472-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="6c472-169">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="6c472-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="6c472-170">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="6c472-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="6c472-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6c472-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6c472-172">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6c472-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="6c472-173">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="6c472-173">Filter CLSID</span></span>

<span data-ttu-id="6c472-174">**CLSID \_ de CMPEG2AudDecoderDS** (declarado en wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="6c472-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="6c472-175">Executable</span><span class="sxs-lookup"><span data-stu-id="6c472-175">Executable</span></span>

<span data-ttu-id="6c472-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="6c472-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="6c472-177">Fundament</span><span class="sxs-lookup"><span data-stu-id="6c472-177">Merit</span></span>](merit.md)

<span data-ttu-id="6c472-178">**Mérito \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="6c472-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="6c472-179">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="6c472-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="6c472-180">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="6c472-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="6c472-181">Una versión anterior de la documentación indicó que este filtro puede descodificar "audio MPEG-2".</span><span class="sxs-lookup"><span data-stu-id="6c472-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="6c472-182">El filtro descodifica solo audio MPEG-2 compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="6c472-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="6c472-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c472-183">Remarks</span></span>

<span data-ttu-id="6c472-184">Los flujos mono siempre se descodifican en estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c472-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="6c472-185">En el caso de las secuencias con una configuración de canal de dos o más oradores, el descodificador realiza una de las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c472-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="6c472-186">Se mezcla hasta seis canales mediante la configuración de altavoz común 5,1.</span><span class="sxs-lookup"><span data-stu-id="6c472-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="6c472-187">Downmixes a estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c472-187">Downmixes to stereo.</span></span>

<span data-ttu-id="6c472-188">Para seleccionar entre estas dos opciones, use la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para establecer la propiedad [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) antes de conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="6c472-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="6c472-189">Como alternativa, cuando la aplicación genera el gráfico de filtro, puede establecer el tipo de medio deseado en el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="6c472-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="6c472-190">Descodificación AAC</span><span class="sxs-lookup"><span data-stu-id="6c472-190">AAC Decoding</span></span>

<span data-ttu-id="6c472-191">Para AAC, el descodificador tiene ciertas restricciones de formato en la entrada AAC comprimida.</span><span class="sxs-lookup"><span data-stu-id="6c472-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="6c472-192">Estas restricciones de formato son las mismas que las del [**descodificador AAC**](../medfound/aac-decoder.md)Media Foundation y se documentan en la sección "[**restricciones de formato**](../medfound/aac-decoder.md)".</span><span class="sxs-lookup"><span data-stu-id="6c472-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="6c472-193">El descodificador de DirectShow también acepta distintos tipos de entrada que el descodificador de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6c472-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="6c472-194">El descodificador de DirectShow admite los siguientes tipos de entrada AAC:</span><span class="sxs-lookup"><span data-stu-id="6c472-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="6c472-195">**MEDIASUBTYPE \_ RAW \_ AAC1**: AAC sin formato, que normalmente se encuentra en AVI o Matroska (. MKV).</span><span class="sxs-lookup"><span data-stu-id="6c472-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="6c472-196">**MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC en una secuencia de transporte de datos de audio (ADTS) para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="6c472-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="6c472-197">**MEDIASUBTYPE \_ MPEG \_ loa**: flujo de transporte con una capa de sincronización (Loa) y una capa de multiplexación (LATM).</span><span class="sxs-lookup"><span data-stu-id="6c472-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="6c472-198">El descodificador de Media Foundation admite los siguientes tipos de entrada AAC:</span><span class="sxs-lookup"><span data-stu-id="6c472-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="6c472-199">MFAudioFormat \_ AAC (igual que **MEDIASUBTYPE \_ MPEG \_ HEAAC**) para la reproducción de archivos MP4.</span><span class="sxs-lookup"><span data-stu-id="6c472-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="6c472-200">**MEDIASUBTYPE \_ \_AAC1 sin formato**.</span><span class="sxs-lookup"><span data-stu-id="6c472-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="6c472-201">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="6c472-201">Property Sets</span></span>

<span data-ttu-id="6c472-202">El PIN de entrada del descodificador admite los siguientes conjuntos de propiedades a través de [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="6c472-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="6c472-203">**Conjunto de propiedades de protección de copia de DVD**</span><span class="sxs-lookup"><span data-stu-id="6c472-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="6c472-204">[**Conjunto de propiedades Rate-Change**](rate-change-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="6c472-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="6c472-205">A partir de Windows 7, el descodificador admite el modo de truco a través del conjunto de propiedades Rate-Change.</span><span class="sxs-lookup"><span data-stu-id="6c472-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="6c472-206">Admite velocidades de reproducción en el intervalo de \[ 0,501 \] a 2,0, donde 1,0 es la velocidad de reproducción normal y 2,0 es el doble de la tarifa normal.</span><span class="sxs-lookup"><span data-stu-id="6c472-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="6c472-207">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="6c472-207">Codec Properties</span></span>

<span data-ttu-id="6c472-208">El PIN de entrada del descodificador admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="6c472-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="6c472-209">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c472-209">Property</span></span>                                                          | <span data-ttu-id="6c472-210">Requiere</span><span class="sxs-lookup"><span data-stu-id="6c472-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6c472-211">**AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="6c472-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="6c472-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="6c472-213">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="6c472-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="6c472-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="6c472-215">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="6c472-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="6c472-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="6c472-217">**AVDDSurroundMode**</span><span class="sxs-lookup"><span data-stu-id="6c472-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="6c472-218">Solo Windows Vista; no se admite en Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6c472-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="6c472-219">**AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="6c472-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="6c472-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="6c472-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="6c472-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="6c472-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="6c472-223">**AVDecCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="6c472-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="6c472-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c472-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="6c472-225">El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="6c472-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="6c472-226">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c472-226">Property</span></span>                                                                          | <span data-ttu-id="6c472-227">Requiere</span><span class="sxs-lookup"><span data-stu-id="6c472-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="6c472-228">**AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="6c472-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="6c472-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c472-229">Windows 7</span></span>     |
| [<span data-ttu-id="6c472-230">**AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="6c472-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="6c472-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-231">Windows Vista</span></span> |
| <span data-ttu-id="6c472-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (véase la nota 3).</span><span class="sxs-lookup"><span data-stu-id="6c472-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="6c472-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-233">Windows Vista</span></span> |
| [<span data-ttu-id="6c472-234">**AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="6c472-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="6c472-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-235">Windows Vista</span></span> |
| [<span data-ttu-id="6c472-236">**AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="6c472-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="6c472-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-237">Windows Vista</span></span> |
| [<span data-ttu-id="6c472-238">**AVDecDDOperationalMode**</span><span class="sxs-lookup"><span data-stu-id="6c472-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="6c472-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-239">Windows Vista</span></span> |
| [<span data-ttu-id="6c472-240">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="6c472-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="6c472-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c472-241">Windows Vista</span></span> |
| [<span data-ttu-id="6c472-242">**AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="6c472-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="6c472-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c472-243">Windows 7</span></span>     |
| [<span data-ttu-id="6c472-244">**AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="6c472-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="6c472-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c472-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="6c472-246">La propiedad [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) debe establecerse antes de que se conecte el PIN de salida del descodificador.</span><span class="sxs-lookup"><span data-stu-id="6c472-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="6c472-247">De lo contrario, el cambio no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="6c472-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c472-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c472-248">Requirements</span></span>



| <span data-ttu-id="6c472-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c472-249">Requirement</span></span> | <span data-ttu-id="6c472-250">Value</span><span class="sxs-lookup"><span data-stu-id="6c472-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c472-251">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c472-251">Minimum supported client</span></span><br/> | <span data-ttu-id="6c472-252">Windows Vista Home Premium, Windows Vista Ultimate, solo para aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c472-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6c472-253">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c472-253">Minimum supported server</span></span><br/> | <span data-ttu-id="6c472-254">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6c472-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6c472-255">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c472-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c472-256"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c472-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="6c472-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c472-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c472-258">**Subtipos de audio**</span><span class="sxs-lookup"><span data-stu-id="6c472-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="6c472-259">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c472-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="6c472-260">**Tipos de medios de DVD**</span><span class="sxs-lookup"><span data-stu-id="6c472-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
