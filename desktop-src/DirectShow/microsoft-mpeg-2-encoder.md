---
description: El filtro del codificador MPEG-2 de Microsoft codifica el audio y el vídeo MPEG-2 y multiplexa los flujos para generar una secuencia de transporte o flujo de programa MPEG-2.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Codificador MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805624"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="d7311-103">Codificador MPEG-2 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d7311-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="d7311-104">El filtro del codificador MPEG-2 de Microsoft codifica el audio y el vídeo MPEG-2 y multiplexa los flujos para generar una secuencia de transporte o flujo de programa MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d7311-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="d7311-105">Este filtro no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="d7311-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="d7311-106">Información de filtro</span><span class="sxs-lookup"><span data-stu-id="d7311-106">Filter Information</span></span>

<span data-ttu-id="d7311-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="d7311-107">Filter Interfaces</span></span>

[<span data-ttu-id="d7311-108">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d7311-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="d7311-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d7311-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="d7311-110">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="d7311-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="d7311-111">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="d7311-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="d7311-112">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="d7311-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="d7311-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="d7311-113">Input Pin Media Types</span></span>

<span data-ttu-id="d7311-114">Ver comentarios</span><span class="sxs-lookup"><span data-stu-id="d7311-114">See Remarks</span></span>

<span data-ttu-id="d7311-115">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="d7311-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="d7311-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="d7311-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="d7311-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="d7311-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="d7311-118">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="d7311-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="d7311-119">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="d7311-119">Output Pin Media Types</span></span>

<span data-ttu-id="d7311-120">Ver comentarios</span><span class="sxs-lookup"><span data-stu-id="d7311-120">See Remarks</span></span>

<span data-ttu-id="d7311-121">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="d7311-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="d7311-122">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="d7311-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="d7311-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="d7311-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="d7311-124">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="d7311-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="d7311-125">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="d7311-125">Filter CLSID</span></span>

<span data-ttu-id="d7311-126">**CLSID \_ de CMPEG2EncoderDS** (declarado en wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="d7311-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="d7311-127">Executable</span><span class="sxs-lookup"><span data-stu-id="d7311-127">Executable</span></span>

<span data-ttu-id="d7311-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="d7311-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="d7311-129">Fundament</span><span class="sxs-lookup"><span data-stu-id="d7311-129">Merit</span></span>](merit.md)

<span data-ttu-id="d7311-130">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="d7311-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="d7311-131">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="d7311-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="d7311-132">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="d7311-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="d7311-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7311-133">Remarks</span></span>

<span data-ttu-id="d7311-134">Este filtro combina la funcionalidad de codificación de otros dos filtros:</span><span class="sxs-lookup"><span data-stu-id="d7311-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="d7311-135">**Codificador de audio MPEG-2 de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="d7311-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="d7311-136">**Codificador de vídeo MPEG-2 de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="d7311-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="d7311-137">A menos que se indique lo contrario, este filtro admite las mismas características de codificación que los dos codificadores.</span><span class="sxs-lookup"><span data-stu-id="d7311-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="d7311-138">Inicialmente, el filtro tiene un PIN de entrada, que puede aceptar la entrada de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7311-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="d7311-139">Cuando el PIN está conectado, el filtro crea un segundo PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7311-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="d7311-140">Si el primer PIN de entrada recibe audio, el segundo PIN de entrada solo acepta vídeo y viceversa.</span><span class="sxs-lookup"><span data-stu-id="d7311-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="d7311-141">Cada pin de entrada admite los mismos tipos de medios que el filtro de codificador correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d7311-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="d7311-142">Si solo hay un PIN de entrada conectado, el filtro admite los mismos tipos de salida que el codificador de audio o vídeo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d7311-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="d7311-143">Si ambos PIN están conectados, el filtro admite los siguientes tipos de resultados:</span><span class="sxs-lookup"><span data-stu-id="d7311-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="d7311-144">Audio-visual en una secuencia de programa MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d7311-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="d7311-145">Audio-visual en una secuencia de transporte MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d7311-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="d7311-146">Estos se corresponden con los siguientes tipos de salida:</span><span class="sxs-lookup"><span data-stu-id="d7311-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="d7311-147">**MEDIATYPE \_ Stream**, **\_ \_ programa MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d7311-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="d7311-148">**MEDIATYPE \_ Stream**, **\_ \_ transporte MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d7311-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="d7311-149">Este filtro no puede multiplexar flujos previamente codificados.</span><span class="sxs-lookup"><span data-stu-id="d7311-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="d7311-150">Los flujos de entrada deben ser audio/vídeo sin comprimir, que el filtro codifica antes de multiplexar.</span><span class="sxs-lookup"><span data-stu-id="d7311-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="d7311-151">La secuencia multiplexada está limitada a un programa que contiene hasta un audio y un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7311-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="d7311-152">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="d7311-152">Codec Properties</span></span>

<span data-ttu-id="d7311-153">El filtro admite las propiedades combinadas del [**codificador de audio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) y los filtros del [**codificador de vídeo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , con la siguiente diferencia:</span><span class="sxs-lookup"><span data-stu-id="d7311-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="d7311-154">La propiedad [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) establece la velocidad de bits promedio para el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7311-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="d7311-155">La propiedad [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) establece la velocidad de bits promedio para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="d7311-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7311-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7311-156">Requirements</span></span>



| <span data-ttu-id="d7311-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7311-157">Requirement</span></span> | <span data-ttu-id="d7311-158">Value</span><span class="sxs-lookup"><span data-stu-id="d7311-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7311-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7311-159">Minimum supported client</span></span><br/> | <span data-ttu-id="d7311-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d7311-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7311-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7311-161">Minimum supported server</span></span><br/> | <span data-ttu-id="d7311-162">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7311-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="d7311-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7311-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7311-164"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7311-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="d7311-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7311-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7311-166">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7311-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
