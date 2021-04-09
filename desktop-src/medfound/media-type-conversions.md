---
description: Conversiones de tipos de medios
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversiones de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820311"
---
# <a name="media-type-conversions"></a><span data-ttu-id="8879e-103">Conversiones de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="8879e-103">Media Type Conversions</span></span>

<span data-ttu-id="8879e-104">En ocasiones, es necesario convertir entre Media Foundation tipos de medios y las estructuras de tipos de medios anteriores de DirectShow o el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="8879e-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="8879e-105">De una estructura de formato a un tipo de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8879e-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="8879e-106">Las siguientes funciones inicializan un tipo de medio Media Foundation a partir de una estructura de formato.</span><span class="sxs-lookup"><span data-stu-id="8879e-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="8879e-107">Estas funciones también son útiles si un flujo de datos o un encabezado de archivo contiene una estructura de formato.</span><span class="sxs-lookup"><span data-stu-id="8879e-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="8879e-108">Por ejemplo, el encabezado de archivo de los archivos de audio de WAVE contiene una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8879e-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8879e-109">Estructura que se va a convertir</span><span class="sxs-lookup"><span data-stu-id="8879e-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="8879e-110">Función</span><span class="sxs-lookup"><span data-stu-id="8879e-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8879e-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="8879e-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="8879e-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objetos multimedia de DirectX)</span><span class="sxs-lookup"><span data-stu-id="8879e-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="8879e-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (SDK de Windows Media Format)</span><span class="sxs-lookup"><span data-stu-id="8879e-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8879e-114">Estas estructuras son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8879e-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="8879e-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8879e-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="8879e-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8879e-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="8879e-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8879e-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="8879e-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8879e-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="8879e-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8879e-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="8879e-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8879e-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="8879e-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8879e-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> o <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="8879e-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8879e-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="8879e-130">Desde un Media Foundation tipo a una estructura de formato</span><span class="sxs-lookup"><span data-stu-id="8879e-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="8879e-131">Las siguientes funciones crean o inicializan una estructura de formato a partir de un tipo de medio Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8879e-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="8879e-132">Función</span><span class="sxs-lookup"><span data-stu-id="8879e-132">Function</span></span>                                                                             | <span data-ttu-id="8879e-133">Estructura de destino</span><span class="sxs-lookup"><span data-stu-id="8879e-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8879e-134">**IMFMediaType::GetRepresentation**</span><span class="sxs-lookup"><span data-stu-id="8879e-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="8879e-135">[**AM \_ \_Tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="8879e-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="8879e-136">**MFCreateAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8879e-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="8879e-137">**\_tipo de medio am \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="8879e-138">**MFCreateMFVideoFormatFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8879e-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="8879e-139">**MFVIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="8879e-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="8879e-140">**MFCreateWaveFormatExFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8879e-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="8879e-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8879e-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="8879e-142">**MFInitAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8879e-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="8879e-143">**\_tipo de medio am \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="8879e-144">Asignaciones de formato</span><span class="sxs-lookup"><span data-stu-id="8879e-144">Format Mappings</span></span>

<span data-ttu-id="8879e-145">En las tablas siguientes se enumeran los atributos de Media Foundation que corresponden a varias estructuras de formato.</span><span class="sxs-lookup"><span data-stu-id="8879e-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="8879e-146">No todos estos atributos se pueden traducir directamente.</span><span class="sxs-lookup"><span data-stu-id="8879e-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="8879e-147">Para realizar conversiones, debe utilizar las funciones enumeradas en la sección anterior; Estas tablas se proporcionan principalmente como referencia.</span><span class="sxs-lookup"><span data-stu-id="8879e-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="8879e-148">\_tipo de medio am \_</span><span class="sxs-lookup"><span data-stu-id="8879e-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="8879e-149">Member</span><span class="sxs-lookup"><span data-stu-id="8879e-149">Member</span></span>                   | <span data-ttu-id="8879e-150">Atributo</span><span class="sxs-lookup"><span data-stu-id="8879e-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8879e-151">**bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="8879e-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="8879e-152">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="8879e-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="8879e-153">**bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="8879e-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="8879e-154">**\_ejemplos de \_ \_ tamaño fijo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="8879e-155">**lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="8879e-155">**lSampleSize**</span></span>          | [<span data-ttu-id="8879e-156">**tamaño de muestra de MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="8879e-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="8879e-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="8879e-158">Member</span><span class="sxs-lookup"><span data-stu-id="8879e-158">Member</span></span>                  | <span data-ttu-id="8879e-159">Atributo</span><span class="sxs-lookup"><span data-stu-id="8879e-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8879e-160">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="8879e-160">**wFormatTag**</span></span>          | [<span data-ttu-id="8879e-161">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="8879e-162">Si **wFormatTag** es \_ \_ extensible, el subtipo se encuentra en el miembro del **subformato** .</span><span class="sxs-lookup"><span data-stu-id="8879e-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="8879e-163">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="8879e-163">**nChannels**</span></span>           | [<span data-ttu-id="8879e-164">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="8879e-165">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="8879e-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="8879e-166">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="8879e-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="8879e-167">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="8879e-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="8879e-168">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="8879e-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="8879e-169">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="8879e-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="8879e-170">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="8879e-171">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="8879e-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="8879e-172">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="8879e-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="8879e-173">**wValidBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="8879e-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="8879e-174">**\_ \_ bits válidos de audio MF MT \_ \_ \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="8879e-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="8879e-175">**wSamplesPerBlock**</span><span class="sxs-lookup"><span data-stu-id="8879e-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="8879e-176">**\_ejemplos de audio MF MT \_ \_ \_ por \_ bloque**</span><span class="sxs-lookup"><span data-stu-id="8879e-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="8879e-177">**dwChannelMask**</span><span class="sxs-lookup"><span data-stu-id="8879e-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="8879e-178">**\_máscara de \_ canal de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="8879e-179">**SubFormat**</span><span class="sxs-lookup"><span data-stu-id="8879e-179">**SubFormat**</span></span>           | [<span data-ttu-id="8879e-180">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="8879e-181">Datos adicionales</span><span class="sxs-lookup"><span data-stu-id="8879e-181">Extra data</span></span>              | [<span data-ttu-id="8879e-182">**datos de usuario de MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="8879e-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="8879e-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="8879e-184">Member</span><span class="sxs-lookup"><span data-stu-id="8879e-184">Member</span></span>                                         | <span data-ttu-id="8879e-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="8879e-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8879e-186">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="8879e-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="8879e-187">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="8879e-188">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="8879e-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="8879e-189">**\_tasa de \_ \_ errores de bit medio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="8879e-190">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="8879e-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="8879e-191">[**MF \_ \_ \_ Velocidad de fotogramas de MT**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) para calcular este valor.</span><span class="sxs-lookup"><span data-stu-id="8879e-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="8879e-192">**dwInterlaceFlags**</span><span class="sxs-lookup"><span data-stu-id="8879e-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="8879e-193">**\_ \_ modo entrelazado MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="8879e-194">**dwCopyProtectFlags**</span><span class="sxs-lookup"><span data-stu-id="8879e-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="8879e-195">No hay ningún equivalente definido</span><span class="sxs-lookup"><span data-stu-id="8879e-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="8879e-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span><span class="sxs-lookup"><span data-stu-id="8879e-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="8879e-197">[**MF \_ \_Proporción de \_ aspecto \_ de píxeles de MT**](mf-mt-pixel-aspect-ratio-attribute.md); debe convertirse de la relación de aspecto de imagen en la relación de aspecto de imagen.</span><span class="sxs-lookup"><span data-stu-id="8879e-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="8879e-198">**dwControlFlags**</span><span class="sxs-lookup"><span data-stu-id="8879e-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="8879e-199">[**MF \_ \_marcas de \_ control \_ Pad de MT**](mf-mt-pad-control-flags-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="8879e-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="8879e-200">Si está presente la marca **AMCONTROL \_ COLORINFO \_ present** , establezca los atributos de color extendido descritos en [información de color ampliada](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="8879e-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="8879e-201">**bmiHeader. biwidth**, **BmiHeader. biheight**</span><span class="sxs-lookup"><span data-stu-id="8879e-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="8879e-202">**\_tamaño de \_ marco MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="8879e-203">**bmiHeader.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="8879e-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="8879e-204">Implícito en el subtipo ([**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="8879e-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="8879e-205">**bmiHeader. bicompression**</span><span class="sxs-lookup"><span data-stu-id="8879e-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="8879e-206">Implícito en el subtipo.</span><span class="sxs-lookup"><span data-stu-id="8879e-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="8879e-207">**bmiHeader.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="8879e-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="8879e-208">**tamaño de muestra de MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="8879e-209">Información de la paleta</span><span class="sxs-lookup"><span data-stu-id="8879e-209">Palette information</span></span>                            | [<span data-ttu-id="8879e-210">**\_paleta MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="8879e-211">Los siguientes atributos se pueden inferir de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , pero también requieren cierto conocimiento de los detalles del formato.</span><span class="sxs-lookup"><span data-stu-id="8879e-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="8879e-212">Por ejemplo, los distintos formatos YUV tienen diferentes requisitos de STRIDE.</span><span class="sxs-lookup"><span data-stu-id="8879e-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="8879e-213">**\_ \_ intervalo predeterminado de MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="8879e-214">**\_ \_ apertura mínima de \_ pantalla MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="8879e-215">**\_apertura de \_ \_ análisis panorámico MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="8879e-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="8879e-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="8879e-217">Member</span><span class="sxs-lookup"><span data-stu-id="8879e-217">Member</span></span>                                   | <span data-ttu-id="8879e-218">Atributo</span><span class="sxs-lookup"><span data-stu-id="8879e-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8879e-219">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="8879e-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="8879e-220">**\_código de \_ \_ hora de inicio de MPEG MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="8879e-221">**bSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="8879e-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="8879e-222">**\_encabezado de secuencia MF MT \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="8879e-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="8879e-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="8879e-224">**\_relación de \_ aspecto de píxeles MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="8879e-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="8879e-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="8879e-226">Member</span><span class="sxs-lookup"><span data-stu-id="8879e-226">Member</span></span>               | <span data-ttu-id="8879e-227">Atributo</span><span class="sxs-lookup"><span data-stu-id="8879e-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8879e-228">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="8879e-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="8879e-229">**\_código de \_ \_ hora de inicio de MPEG MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="8879e-230">**dwSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="8879e-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="8879e-231">**\_encabezado de secuencia MF MT \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="8879e-232">**dwProfile**</span><span class="sxs-lookup"><span data-stu-id="8879e-232">**dwProfile**</span></span>        | [<span data-ttu-id="8879e-233">**\_Perfil MF MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="8879e-234">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="8879e-234">**dwLevel**</span></span>          | [<span data-ttu-id="8879e-235">**\_Nivel MF MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="8879e-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="8879e-236">**dwFlags**</span></span>          | [<span data-ttu-id="8879e-237">**Marcas de MF \_ MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8879e-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="8879e-238">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8879e-238">Examples</span></span>

<span data-ttu-id="8879e-239">En el código siguiente se rellena una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) a partir de un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8879e-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="8879e-240">Tenga en cuenta que esta conversión pierde parte de la información de formato (entrelazado, velocidad de fotogramas, datos de color extendido).</span><span class="sxs-lookup"><span data-stu-id="8879e-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="8879e-241">Sin embargo, podría ser útil al guardar un mapa de bits de un fotograma de vídeo, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8879e-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8879e-242">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8879e-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8879e-243">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="8879e-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
