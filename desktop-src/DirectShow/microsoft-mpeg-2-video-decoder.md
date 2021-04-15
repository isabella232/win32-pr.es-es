---
description: Este filtro descodifica el vídeo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Descodificador de vídeo MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422802"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="6631b-103">Descodificador de vídeo MPEG-2 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6631b-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="6631b-104">Este filtro descodifica el vídeo MPEG-1, MPEG-2, H. 264.</span><span class="sxs-lookup"><span data-stu-id="6631b-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="6631b-105">La descodificación del vídeo H. 264 requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6631b-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6631b-106">Este filtro no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="6631b-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="6631b-107">En el registro, el nombre descriptivo de este filtro es "Microsoft DTV-DVD video descodificador".</span><span class="sxs-lookup"><span data-stu-id="6631b-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="6631b-108">Información de filtro</span><span class="sxs-lookup"><span data-stu-id="6631b-108">Filter Information</span></span>

<span data-ttu-id="6631b-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="6631b-109">Filter Interfaces</span></span>

[<span data-ttu-id="6631b-110">**IAMDecoderCaps**</span><span class="sxs-lookup"><span data-stu-id="6631b-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="6631b-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6631b-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="6631b-112">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6631b-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="6631b-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="6631b-113">Input Pin Media Types</span></span>

<span data-ttu-id="6631b-114">PIN de entrada de vídeo:</span><span class="sxs-lookup"><span data-stu-id="6631b-114">Video input pin:</span></span>

-   <span data-ttu-id="6631b-115">\_ \_ Paquete cifrado \_ de DVD de MEDIATYPE, vídeo de MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="6631b-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="6631b-116">\_Vídeo MPEG2 \_ de MEDIATYPE, MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="6631b-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="6631b-117">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="6631b-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="6631b-118">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="6631b-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="6631b-119">Vídeo \_ de MEDIATYPE, \_ vídeo de MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="6631b-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="6631b-120">PIN de entrada de subimagen:</span><span class="sxs-lookup"><span data-stu-id="6631b-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="6631b-121">MEDIATYPE \_ \_ paquete cifrado \_ de DVD, MEDIASUBTYPE \_ DVD \_ subpicture</span><span class="sxs-lookup"><span data-stu-id="6631b-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="6631b-122">A partir de Windows 7, el PIN de entrada de vídeo también admite los siguientes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="6631b-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="6631b-123">**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ avc1**</span><span class="sxs-lookup"><span data-stu-id="6631b-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="6631b-124">**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="6631b-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="6631b-125">**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="6631b-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="6631b-126">**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="6631b-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="6631b-127">**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="6631b-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="6631b-128">Para obtener más información, consulte [tipos de vídeo H. 264](h-264-video-types.md) .</span><span class="sxs-lookup"><span data-stu-id="6631b-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="6631b-129">El tipo de medio de entrada puede cambiar dinámicamente entre los tipos de MPEG2 y H. 264.</span><span class="sxs-lookup"><span data-stu-id="6631b-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="6631b-130">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="6631b-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="6631b-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6631b-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="6631b-132">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="6631b-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="6631b-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="6631b-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="6631b-134">**IMFSampleProtection**</span><span class="sxs-lookup"><span data-stu-id="6631b-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="6631b-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6631b-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6631b-136">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6631b-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="6631b-137">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="6631b-137">Output Pin Media Types</span></span>

<span data-ttu-id="6631b-138">PIN de salida de vídeo:</span><span class="sxs-lookup"><span data-stu-id="6631b-138">Video output pin:</span></span>

-   <span data-ttu-id="6631b-139">Vídeo de MEDIATYPE \_ , DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="6631b-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="6631b-140">\_Vídeo de MEDIATYPE, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="6631b-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="6631b-141">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ i420 (descodificación de software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="6631b-142">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ NV12 (descodificación de software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="6631b-143">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ YUY2 (descodificación de software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="6631b-144">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ IMC3 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="6631b-145">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ IMC4 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="6631b-146">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ S340 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="6631b-147">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ YV12 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="6631b-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="6631b-148">PIN de salida de línea 21:</span><span class="sxs-lookup"><span data-stu-id="6631b-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="6631b-149">MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket</span><span class="sxs-lookup"><span data-stu-id="6631b-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="6631b-150">PIN de salida de la subimagen:</span><span class="sxs-lookup"><span data-stu-id="6631b-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="6631b-151">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="6631b-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="6631b-152">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="6631b-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="6631b-153">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="6631b-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="6631b-154">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="6631b-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="6631b-155">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="6631b-155">Output Pin Interfaces</span></span>

<span data-ttu-id="6631b-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo PIN de salida de vídeo)</span><span class="sxs-lookup"><span data-stu-id="6631b-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="6631b-157">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="6631b-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="6631b-158">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="6631b-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="6631b-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6631b-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6631b-160">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6631b-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="6631b-161">**IVPConfig**</span><span class="sxs-lookup"><span data-stu-id="6631b-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="6631b-162">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="6631b-162">Filter CLSID</span></span>

<span data-ttu-id="6631b-163">**CLSID \_ de CMPEG2VidDecoderDS** (definido en wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="6631b-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="6631b-164">Executable</span><span class="sxs-lookup"><span data-stu-id="6631b-164">Executable</span></span>

<span data-ttu-id="6631b-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="6631b-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="6631b-166">Fundament</span><span class="sxs-lookup"><span data-stu-id="6631b-166">Merit</span></span>](merit.md)

<span data-ttu-id="6631b-167">**Mérito \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="6631b-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="6631b-168">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="6631b-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="6631b-169">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="6631b-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="6631b-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6631b-170">Remarks</span></span>

<span data-ttu-id="6631b-171">Este filtro tiene dos clavijas de entrada y tres clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="6631b-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="6631b-172">Clavijas de entrada:</span><span class="sxs-lookup"><span data-stu-id="6631b-172">Input pins:</span></span>

-   <span data-ttu-id="6631b-173">Entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="6631b-173">Video input</span></span>
-   <span data-ttu-id="6631b-174">Entrada de subimagen</span><span class="sxs-lookup"><span data-stu-id="6631b-174">Subpicture input</span></span>

<span data-ttu-id="6631b-175">Clavijas de salida:</span><span class="sxs-lookup"><span data-stu-id="6631b-175">Output pins:</span></span>

-   <span data-ttu-id="6631b-176">Salida de vídeo</span><span class="sxs-lookup"><span data-stu-id="6631b-176">Video output</span></span>
-   <span data-ttu-id="6631b-177">Salida de line-21</span><span class="sxs-lookup"><span data-stu-id="6631b-177">Line-21 output</span></span>
-   <span data-ttu-id="6631b-178">Salida de la subimagen</span><span class="sxs-lookup"><span data-stu-id="6631b-178">Subpicture output</span></span>

<span data-ttu-id="6631b-179">El filtro no crea el PIN de salida de la subimagen a menos que la clavija de entrada de vídeo esté conectada con un tipo de medio de **\_ \_ \_ paquete cifrado de DVD de MEDIATYPE** .</span><span class="sxs-lookup"><span data-stu-id="6631b-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="6631b-180">Compatibilidad con MPEG-1/2</span><span class="sxs-lookup"><span data-stu-id="6631b-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="6631b-181">En MPEG-1 y MPEG-2, el descodificador admite los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="6631b-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6631b-182">Perfiles/niveles</span><span class="sxs-lookup"><span data-stu-id="6631b-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="6631b-183">Cualquier combinación de los siguientes perfiles y niveles:</span><span class="sxs-lookup"><span data-stu-id="6631b-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="6631b-184">Perfiles: simple, principal</span><span class="sxs-lookup"><span data-stu-id="6631b-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="6631b-185">Niveles: bajo, principal, alto y alto 1440</span><span class="sxs-lookup"><span data-stu-id="6631b-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6631b-186">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="6631b-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="6631b-187">croma 4:2:0</span><span class="sxs-lookup"><span data-stu-id="6631b-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6631b-188">Resolución máxima</span><span class="sxs-lookup"><span data-stu-id="6631b-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="6631b-189">1920 × 1088 píxeles</span><span class="sxs-lookup"><span data-stu-id="6631b-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6631b-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="6631b-190">DXVA</span></span></td>
<td><span data-ttu-id="6631b-191">El descodificador admite DirectX video Acceleration (DXVA) versión 1 y versión 2.</span><span class="sxs-lookup"><span data-stu-id="6631b-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6631b-192">El descodificador no admite bitstreams escalables.</span><span class="sxs-lookup"><span data-stu-id="6631b-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="6631b-193">La entrada debe ser una secuencia de vídeo elemental.</span><span class="sxs-lookup"><span data-stu-id="6631b-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="6631b-194">El descodificador no admite formatos de croma de 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="6631b-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="6631b-195">Compatibilidad con H. 264</span><span class="sxs-lookup"><span data-stu-id="6631b-195">H.264 Support</span></span>

<span data-ttu-id="6631b-196">Para H. 264, el descodificador admite los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="6631b-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="6631b-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="6631b-197">Requirement</span></span> | <span data-ttu-id="6631b-198">Value</span><span class="sxs-lookup"><span data-stu-id="6631b-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6631b-199">Perfiles/niveles</span><span class="sxs-lookup"><span data-stu-id="6631b-199">Profiles/Levels</span></span>    | <span data-ttu-id="6631b-200">Perfiles de línea base, principal y alto, hasta el nivel 5,1.</span><span class="sxs-lookup"><span data-stu-id="6631b-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="6631b-201">(Consulte Especificación de ITU-T H. 264 para más información).</span><span class="sxs-lookup"><span data-stu-id="6631b-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="6631b-202">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="6631b-202">Chroma Formats</span></span>     | <span data-ttu-id="6631b-203">4:2:0 croma o monocromo</span><span class="sxs-lookup"><span data-stu-id="6631b-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="6631b-204">Resolución mínima</span><span class="sxs-lookup"><span data-stu-id="6631b-204">Minimum Resolution</span></span> | <span data-ttu-id="6631b-205">48 × 48 píxeles</span><span class="sxs-lookup"><span data-stu-id="6631b-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6631b-206">Resolución máxima</span><span class="sxs-lookup"><span data-stu-id="6631b-206">Maximum Resolution</span></span> | <span data-ttu-id="6631b-207">1920 × 1088 píxeles</span><span class="sxs-lookup"><span data-stu-id="6631b-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6631b-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="6631b-208">DXVA</span></span>               | <span data-ttu-id="6631b-209">El descodificador admite DXVA versión 2, pero no la versión 1 de DXVA.</span><span class="sxs-lookup"><span data-stu-id="6631b-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="6631b-210">La descodificación de DXVA solo se admite para la bitstreams de línea de base, principal y de perfil alto compatible con Main.</span><span class="sxs-lookup"><span data-stu-id="6631b-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="6631b-211">(Las bitstreams de línea de base compatibles con Main se definen como el **perfil \_ idc**= 66 y la **\_ \_ marca de Set1 restringida**= 1).</span><span class="sxs-lookup"><span data-stu-id="6631b-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="6631b-212">El descodificador no admite la tecnología de grano de películas.</span><span class="sxs-lookup"><span data-stu-id="6631b-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="6631b-213">Para obtener información sobre los tipos de medios H. 264, consulte [tipos de vídeo h. 264](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="6631b-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="6631b-214">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="6631b-214">Codec Properties</span></span>

<span data-ttu-id="6631b-215">Los pin de entrada admiten los siguientes conjuntos de propiedades a través de [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="6631b-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="6631b-216">**Conjunto de propiedades de protección de copia de DVD**</span><span class="sxs-lookup"><span data-stu-id="6631b-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="6631b-217">[**Conjunto de propiedades de subimagen de DVD**](dvd-subpicture-property-set.md) (solo PIN de subimagen)</span><span class="sxs-lookup"><span data-stu-id="6631b-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="6631b-218">Los pin de entrada admiten las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="6631b-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="6631b-219">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6631b-219">Property</span></span>                                                                  | <span data-ttu-id="6631b-220">Requiere</span><span class="sxs-lookup"><span data-stu-id="6631b-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="6631b-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="6631b-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="6631b-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6631b-222">Windows Vista</span></span> |
| [<span data-ttu-id="6631b-223">**AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="6631b-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="6631b-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6631b-224">Windows Vista</span></span> |
| [<span data-ttu-id="6631b-225">**AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="6631b-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="6631b-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6631b-226">Windows Vista</span></span> |



 

<span data-ttu-id="6631b-227">El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="6631b-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="6631b-228">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6631b-228">Property</span></span>                                                                                | <span data-ttu-id="6631b-229">Requiere</span><span class="sxs-lookup"><span data-stu-id="6631b-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="6631b-230">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="6631b-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="6631b-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6631b-231">Windows Vista</span></span> |
| [<span data-ttu-id="6631b-232">**AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="6631b-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="6631b-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-233">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-234">**AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="6631b-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="6631b-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-235">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-236">**AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="6631b-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="6631b-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-237">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-238">**AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="6631b-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="6631b-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-239">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-240">**AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="6631b-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="6631b-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-241">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-242">**AVDecVideoSoftwareDeinterlaceMode**</span><span class="sxs-lookup"><span data-stu-id="6631b-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="6631b-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-243">Windows 7</span></span>     |
| [<span data-ttu-id="6631b-244">**AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="6631b-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="6631b-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6631b-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="6631b-246">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6631b-246">Requirements</span></span>



| <span data-ttu-id="6631b-247">Requisito</span><span class="sxs-lookup"><span data-stu-id="6631b-247">Requirement</span></span> | <span data-ttu-id="6631b-248">Value</span><span class="sxs-lookup"><span data-stu-id="6631b-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6631b-249">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6631b-249">Minimum supported client</span></span><br/> | <span data-ttu-id="6631b-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6631b-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6631b-251">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6631b-251">Minimum supported server</span></span><br/> | <span data-ttu-id="6631b-252">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6631b-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="6631b-253">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6631b-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="6631b-254"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6631b-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="6631b-255">Vea también</span><span class="sxs-lookup"><span data-stu-id="6631b-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6631b-256">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6631b-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="6631b-257">**Tipos de medios de DVD**</span><span class="sxs-lookup"><span data-stu-id="6631b-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="6631b-258">Tipos de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="6631b-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
