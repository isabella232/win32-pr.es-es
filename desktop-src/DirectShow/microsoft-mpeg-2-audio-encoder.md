---
description: El filtro del codificador de audio MPEG-2 de Microsoft codifica las capas de audio I y II de MPEG-1, incluida la compatibilidad con las extensiones de la frecuencia de muestreo bajo (LSF) de MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificador de audio MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677113"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="57567-103">Codificador de audio MPEG-2 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="57567-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="57567-104">El filtro del codificador de audio MPEG-2 de Microsoft codifica las capas de audio I y II de MPEG-1, incluida la compatibilidad con las extensiones de la frecuencia de muestreo bajo (LSF) de MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="57567-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="57567-105">Para codificar y multiplexar secuencias de audio/vídeo, use el filtro del [**codificador MPEG-2 de Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula las funciones de este filtro y el filtro del [**codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="57567-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="57567-106">Este filtro no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="57567-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="57567-107">Información de filtro</span><span class="sxs-lookup"><span data-stu-id="57567-107">Filter Information</span></span>

<span data-ttu-id="57567-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="57567-108">Filter Interfaces</span></span>

[<span data-ttu-id="57567-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="57567-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="57567-110">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="57567-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="57567-111">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="57567-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="57567-112">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="57567-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="57567-113">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="57567-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="57567-114">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="57567-114">Input Pin Media Types</span></span>

<span data-ttu-id="57567-115">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="57567-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="57567-116">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="57567-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="57567-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="57567-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="57567-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="57567-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="57567-119">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="57567-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="57567-120">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="57567-120">Output Pin Media Types</span></span>

<span data-ttu-id="57567-121">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="57567-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="57567-122">**MEDIATYPE \_ Streaming**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="57567-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="57567-123">**MEDIATYPE \_ Stream**, **\_ \_ programa MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="57567-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="57567-124">**MEDIATYPE \_ Stream**, **\_ \_ transporte MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="57567-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="57567-125">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="57567-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="57567-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="57567-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="57567-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="57567-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="57567-128">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="57567-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="57567-129">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="57567-129">Filter CLSID</span></span>

<span data-ttu-id="57567-130">**CLSID \_ de CMPEG2EncoderAudioDS** (declarado en wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="57567-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="57567-131">Executable</span><span class="sxs-lookup"><span data-stu-id="57567-131">Executable</span></span>

<span data-ttu-id="57567-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="57567-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="57567-133">Fundament</span><span class="sxs-lookup"><span data-stu-id="57567-133">Merit</span></span>](merit.md)

<span data-ttu-id="57567-134">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="57567-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="57567-135">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="57567-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="57567-136">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="57567-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="57567-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57567-137">Remarks</span></span>

<span data-ttu-id="57567-138">El codificador de audio MPEG-2 puede producir los siguientes tipos de resultados:</span><span class="sxs-lookup"><span data-stu-id="57567-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="57567-139">Secuencia de audio elemental</span><span class="sxs-lookup"><span data-stu-id="57567-139">Audio elementary stream</span></span>
-   <span data-ttu-id="57567-140">Audio en una secuencia de programa MPEG-2</span><span class="sxs-lookup"><span data-stu-id="57567-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="57567-141">Audio en una secuencia de transporte MPEG-2</span><span class="sxs-lookup"><span data-stu-id="57567-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="57567-142">Admite extensiones MPEG-1 Layers I y II y MPEG-2 Low muestreo Frequency (LSF)</span><span class="sxs-lookup"><span data-stu-id="57567-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="57567-143">Los ejemplos de entrada deben tener 16 bits por muestra, con una velocidad de muestreo de audio de 48, 44,1, 32, 22,05 o 16 KHz.</span><span class="sxs-lookup"><span data-stu-id="57567-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="57567-144">El codificador no puede volver a muestrear el flujo de audio; el audio codificado tiene la misma velocidad de muestra que la entrada.</span><span class="sxs-lookup"><span data-stu-id="57567-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="57567-145">Los ejemplos de entrada deben ser mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="57567-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="57567-146">El audio codificado tiene el número de canales como entrada.</span><span class="sxs-lookup"><span data-stu-id="57567-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="57567-147">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="57567-147">Limitations</span></span>

<span data-ttu-id="57567-148">El codificador no admite lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57567-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="57567-149">Bitstreams de audio MPEG Layer III.</span><span class="sxs-lookup"><span data-stu-id="57567-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="57567-150">Bitstreams de extensión de varios canales MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="57567-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="57567-151">Bitstreams AAC MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="57567-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="57567-152">Bitstreams compatible con MPEG-2 (NBC).</span><span class="sxs-lookup"><span data-stu-id="57567-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="57567-153">Generación de paquetes de flujo elemental (PES) de paquetes.</span><span class="sxs-lookup"><span data-stu-id="57567-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="57567-154">Codificación Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="57567-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="57567-155">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="57567-155">Codec Properties</span></span>

<span data-ttu-id="57567-156">El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="57567-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="57567-157">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="57567-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="57567-158">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="57567-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="57567-159">**AVEncAudioIntervalToEncode**</span><span class="sxs-lookup"><span data-stu-id="57567-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="57567-160">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="57567-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="57567-161">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="57567-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="57567-162">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="57567-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="57567-163">**AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="57567-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="57567-164">**AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="57567-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="57567-165">**AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="57567-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="57567-166">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="57567-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="57567-167">**AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="57567-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="57567-168">**AVEncMPAPrivateUserBit**</span><span class="sxs-lookup"><span data-stu-id="57567-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="57567-169">Una versión anterior de la documentación enumeraba incorrectamente algunas propiedades adicionales que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="57567-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="57567-170">Por compatibilidad con versiones anteriores, el filtro admite la siguiente propiedad a través de la interfaz **IEncoderAPI** :</span><span class="sxs-lookup"><span data-stu-id="57567-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="57567-171">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57567-171">Property</span></span>                 | <span data-ttu-id="57567-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="57567-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57567-173">**\_velocidad de bits ENCAPIPARAM**</span><span class="sxs-lookup"><span data-stu-id="57567-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="57567-174">Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span><span class="sxs-lookup"><span data-stu-id="57567-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="57567-175">Se recomienda establecer las propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="57567-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="57567-176">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="57567-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="57567-177">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="57567-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="57567-178">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="57567-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="57567-179">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="57567-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="57567-180">Establezca las propiedades restantes en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="57567-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="57567-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57567-181">Requirements</span></span>



| <span data-ttu-id="57567-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="57567-182">Requirement</span></span> | <span data-ttu-id="57567-183">Value</span><span class="sxs-lookup"><span data-stu-id="57567-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57567-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57567-184">Minimum supported client</span></span><br/> | <span data-ttu-id="57567-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="57567-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="57567-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57567-186">Minimum supported server</span></span><br/> | <span data-ttu-id="57567-187">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="57567-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="57567-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57567-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="57567-189"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57567-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="57567-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="57567-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57567-191">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="57567-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="57567-192">**Tipos de medios de demultiplexador MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="57567-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
