---
description: El descodificador de vídeo H. 264 Media Foundation es una transformación de Media Foundation que admite la descodificación de perfiles de línea base, principales y altos, hasta el nivel 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Descodificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496793"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="f7ff5-103">Descodificador de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="f7ff5-103">H.264 Video Decoder</span></span>

<span data-ttu-id="f7ff5-104">El descodificador de vídeo H. 264 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la descodificación de perfiles de línea base, principales y altos, hasta el nivel 5,1.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="f7ff5-105">El descodificador de vídeo H. 264 expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="f7ff5-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)</span><span class="sxs-lookup"><span data-stu-id="f7ff5-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="f7ff5-107">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="f7ff5-108">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="f7ff5-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="f7ff5-110">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="f7ff5-111">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="f7ff5-112">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="f7ff5-113">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="f7ff5-114">Para crear una instancia del descodificador, realice una de las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7ff5-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="f7ff5-115">Llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="f7ff5-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="f7ff5-116">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="f7ff5-117">El CLSID para el descodificador es **CLSID \_ CMSH264DecoderMFT**, declarado en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="f7ff5-118">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="f7ff5-118">Input Types</span></span>

<span data-ttu-id="f7ff5-119">El tipo de entrada debe contener al menos los dos atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7ff5-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="f7ff5-120">Atributo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-120">Attribute</span></span>                                                 | <span data-ttu-id="f7ff5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ff5-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7ff5-122">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="f7ff5-123">**Vídeo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="f7ff5-124">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="f7ff5-125">[MFVideoFormat \_ H264](video-subtype-guids.md) o MFVideoFormat \_ H264 \_ es</span><span class="sxs-lookup"><span data-stu-id="f7ff5-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="f7ff5-126">Si el tipo de entrada contiene solo estos dos atributos, el descodificador ofrecerá un tipo de salida predeterminado, que actúa como marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="f7ff5-127">Cuando el descodificador recibe suficientes ejemplos de entrada para generar un fotograma de salida, indica un cambio de formato devolviendo el **cambio de secuencia de \_ \_ transformación \_ \_ MF E** de [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="f7ff5-128">Consulte la documentación de **ProcessOutput** para obtener más información sobre el control de los cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="f7ff5-129">Para evitar un cambio de formato inicial, proporcione tanta información como sea posible en el tipo de entrada, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f7ff5-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7ff5-130">Atributo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-130">Attribute</span></span></th>
<th><span data-ttu-id="f7ff5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ff5-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7ff5-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7ff5-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="f7ff5-133">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7ff5-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7ff5-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="f7ff5-135">Dimensiones del marco.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7ff5-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7ff5-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="f7ff5-137">Modo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f7ff5-138">En el vídeo H. 264, la estructura entrelazada puede cambiar dinámicamente, por lo que el valor recomendado de este atributo es <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="f7ff5-139">La información de entrelazado en el flujo elemental de vídeo tiene prioridad sobre el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="f7ff5-140">Para obtener más información, vea <a href="video-interlacing.md">entrelazado de vídeo</a>.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7ff5-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="f7ff5-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="f7ff5-142">Relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f7ff5-143">El tipo de entrada debe establecerse antes que el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-143">The input type must be set before the output type.</span></span> <span data-ttu-id="f7ff5-144">Hasta que se establezca el tipo de entrada, el método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) del codificador devuelve el **tipo de \_ transformación MF E \_ \_ \_ no \_ establecido**.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="f7ff5-145">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="f7ff5-145">Output Types</span></span>

<span data-ttu-id="f7ff5-146">El descodificador admite los siguientes subtipos de salida:</span><span class="sxs-lookup"><span data-stu-id="f7ff5-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="f7ff5-147">**MFVideoFormat \_ i420**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="f7ff5-148">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="f7ff5-149">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="f7ff5-150">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="f7ff5-151">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="f7ff5-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="f7ff5-152">Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="f7ff5-153">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="f7ff5-153">Transform Attributes</span></span>

<span data-ttu-id="f7ff5-154">El descodificador H. 264 implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="f7ff5-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="f7ff5-155">Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="f7ff5-156">Atributo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-156">Attribute</span></span>                                                                                       | <span data-ttu-id="f7ff5-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ff5-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7ff5-158">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="f7ff5-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="f7ff5-159">Habilita o deshabilita la aceleración de hardware.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="f7ff5-160">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="f7ff5-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="f7ff5-161">Habilita o deshabilita el modo de generación de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="f7ff5-162">Compatible con el D3D de MF \_ SA \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7ff5-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="f7ff5-163">Indica que el descodificador admite la aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="f7ff5-164">Tratar como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="f7ff5-165">En Windows 8, el descodificador H. 264 también admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="f7ff5-166">Atributo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="f7ff5-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ff5-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7ff5-168">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="f7ff5-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="f7ff5-169">Habilita o deshabilita el modo de descodificación de latencia baja.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="f7ff5-170">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="f7ff5-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="f7ff5-171">Establece el número de subprocesos de trabajo utilizados por el descodificador.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="f7ff5-172">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="f7ff5-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="f7ff5-173">Establece el ancho máximo de la imagen que el descodificador aceptará como tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="f7ff5-174">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="f7ff5-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="f7ff5-175">Establece el alto máximo de la imagen que el descodificador aceptará como tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="f7ff5-176">recuento de \_ \_ ejemplo de salida mínima de SA de \_ \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="f7ff5-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="f7ff5-177">Especifica el número máximo de ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="f7ff5-178">el \_ DEScodificador \_ de MFT expone \_ \_ tipos \_ de salida en \_ \_ orden nativo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="f7ff5-179">Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="f7ff5-180">En Windows 8, el descodificador H. 264 admite la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="f7ff5-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="f7ff5-181">Esta interfaz proporciona una API alternativate para configurar las siguientes propiedades de códec.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="f7ff5-182">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="f7ff5-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="f7ff5-183">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="f7ff5-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="f7ff5-184">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="f7ff5-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="f7ff5-185">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="f7ff5-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="f7ff5-186">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="f7ff5-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="f7ff5-187">Restricciones de formato</span><span class="sxs-lookup"><span data-stu-id="f7ff5-187">Format Constraints</span></span>

<span data-ttu-id="f7ff5-188">El descodificador admite los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="f7ff5-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7ff5-189">Perfiles/niveles</span><span class="sxs-lookup"><span data-stu-id="f7ff5-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="f7ff5-190">Perfiles de línea base, principal y alto, hasta el nivel 5,1.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="f7ff5-191">(Consulte Especificación de ITU-T H. 264 para más información).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7ff5-192">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="f7ff5-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="f7ff5-193">4:2:0 croma o monocromo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7ff5-194">Resolución mínima</span><span class="sxs-lookup"><span data-stu-id="f7ff5-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="f7ff5-195">48 × 48 píxeles</span><span class="sxs-lookup"><span data-stu-id="f7ff5-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7ff5-196">Resolución máxima</span><span class="sxs-lookup"><span data-stu-id="f7ff5-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="f7ff5-197">4096 × 2304 píxeles</span><span class="sxs-lookup"><span data-stu-id="f7ff5-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="f7ff5-198">La resolución máxima garantizada para la aceleración de DXVA es 1920 × 1088 píxeles; con resoluciones más altas, la descodificación se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, la descodificación se realiza con el software.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f7ff5-199">En Windows 7, la resolución máxima admitida es 1920 × 1088 píxeles para la descodificación de software y de DXVA.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7ff5-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="f7ff5-200">DXVA</span></span></td>
<td><span data-ttu-id="f7ff5-201">El descodificador admite DXVA versión 2, pero no la versión 1 de DXVA.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="f7ff5-202">La descodificación de DXVA solo se admite para la bitstreams de línea de base, principal y de perfil alto compatible con Main.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="f7ff5-203">(Las bitstreams de línea de base compatibles con Main se definen como <strong>profile_idc</strong>= 66 y <strong>constrained_set1_flag</strong>= 1).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f7ff5-204">Los datos de entrada deben ajustarse al Anexo B de ISO/IEC 14496-10.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="f7ff5-205">Los datos deben incluir los códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-205">The data must include the start codes.</span></span> <span data-ttu-id="f7ff5-206">El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) y un conjunto de parámetros de imagen (PPS) válidos en el flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="f7ff5-207">El descodificador no admite la tecnología de grano de películas.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="f7ff5-208">Una versión anterior de la documentación indicó incorrectamente que el descodificador es compatible con Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f7ff5-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="f7ff5-209">Si está instalado el complemento de actualización de plataforma para Windows Vista, el descodificador de vídeo H. 264 está disponible en Windows Vista, pero solo es accesible en Windows Vista mediante el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="f7ff5-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ff5-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7ff5-210">Requirements</span></span>



| <span data-ttu-id="f7ff5-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ff5-211">Requirement</span></span> | <span data-ttu-id="f7ff5-212">Value</span><span class="sxs-lookup"><span data-stu-id="f7ff5-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ff5-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7ff5-213">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ff5-214">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7ff5-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7ff5-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7ff5-215">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ff5-216">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f7ff5-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="f7ff5-217">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7ff5-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7ff5-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ff5-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ff5-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7ff5-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ff5-220">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="f7ff5-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="f7ff5-221">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7ff5-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f7ff5-222">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7ff5-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f7ff5-223">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="f7ff5-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
