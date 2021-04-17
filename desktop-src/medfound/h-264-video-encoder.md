---
description: 'El codificador de vídeo H. 264 Microsoft Media Foundation es una transformación de Media Foundation que admite los siguientes perfiles H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715450"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="9607e-103">Codificador de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="9607e-103">H.264 Video Encoder</span></span>

<span data-ttu-id="9607e-104">El codificador de vídeo H. 264 Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite los siguientes perfiles H. 264:</span><span class="sxs-lookup"><span data-stu-id="9607e-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="9607e-105">Perfil de línea base</span><span class="sxs-lookup"><span data-stu-id="9607e-105">Baseline Profile</span></span>
-   <span data-ttu-id="9607e-106">Perfil Main</span><span class="sxs-lookup"><span data-stu-id="9607e-106">Main Profile</span></span>
-   <span data-ttu-id="9607e-107">Perfil alto (requiere Windows 8)</span><span class="sxs-lookup"><span data-stu-id="9607e-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="9607e-108">El codificador de vídeo H. 264 expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="9607e-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="9607e-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9607e-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="9607e-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="9607e-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="9607e-111">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="9607e-111">Input Types</span></span>

<span data-ttu-id="9607e-112">El tipo de medio de entrada debe tener uno de los siguientes subtipos:</span><span class="sxs-lookup"><span data-stu-id="9607e-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="9607e-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="9607e-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="9607e-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="9607e-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="9607e-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="9607e-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="9607e-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="9607e-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="9607e-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="9607e-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="9607e-118">Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9607e-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="9607e-119">El tipo de salida debe establecerse antes que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="9607e-119">The output type must be set before the input type.</span></span> <span data-ttu-id="9607e-120">Hasta que se establezca el tipo de salida, el método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificador devuelve **MF_E_TRANSFORM_TYPE_NOT_SET**.</span><span class="sxs-lookup"><span data-stu-id="9607e-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="9607e-121">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="9607e-121">Output Types</span></span>

<span data-ttu-id="9607e-122">El codificador admite un solo subtipo de salida:</span><span class="sxs-lookup"><span data-stu-id="9607e-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="9607e-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="9607e-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="9607e-124">Establezca los siguientes atributos en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="9607e-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9607e-125">Atributo</span><span class="sxs-lookup"><span data-stu-id="9607e-125">Attribute</span></span></th>
<th><span data-ttu-id="9607e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9607e-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9607e-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-128">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="9607e-128">Major type.</span></span> <span data-ttu-id="9607e-129">Debe ser <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-131">Subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9607e-131">Video subtype.</span></span> <span data-ttu-id="9607e-132">Debe ser <strong>MFVideoFormat_H264</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-134">Velocidad media de bits codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9607e-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="9607e-135">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="9607e-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-137">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9607e-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-139">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="9607e-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-141">Modo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="9607e-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="9607e-143">Perfil de codificación H. 264.</span><span class="sxs-lookup"><span data-stu-id="9607e-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="9607e-144">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="9607e-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="9607e-145"><strong>eAVEncH264VProfile_Base</strong> (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="9607e-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="9607e-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="9607e-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="9607e-147"><strong>eAVEncH264VProfile_High</strong> (requiere Windows 8)</span><span class="sxs-lookup"><span data-stu-id="9607e-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="9607e-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9607e-149">Optional.</span></span> <span data-ttu-id="9607e-150">Especifica el nivel de codificación H. 264.</span><span class="sxs-lookup"><span data-stu-id="9607e-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="9607e-151">El valor predeterminado es-1, lo que indica que el codificador seleccionará el nivel de codificación.</span><span class="sxs-lookup"><span data-stu-id="9607e-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="9607e-152">Se recomienda no establecer el nivel en el tipo de medio y permitir que el codificador Seleccione el nivel.</span><span class="sxs-lookup"><span data-stu-id="9607e-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="9607e-153">El codificador puede derivar el nivel adecuado para un flujo de vídeo determinado, teniendo en cuenta las restricciones de formato y las características del vídeo.</span><span class="sxs-lookup"><span data-stu-id="9607e-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="9607e-154">Para obtener más información acerca de las restricciones de perfil y de nivel, consulte el anexo a de ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="9607e-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="9607e-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="9607e-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9607e-156">Optional.</span></span> <span data-ttu-id="9607e-157">Especifica la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="9607e-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="9607e-158">El valor predeterminado es 1:1.</span><span class="sxs-lookup"><span data-stu-id="9607e-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9607e-159">Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando el atributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="9607e-160">Este atributo contiene el encabezado de secuencia.</span><span class="sxs-lookup"><span data-stu-id="9607e-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="9607e-161">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="9607e-161">Codec Properties</span></span>

<span data-ttu-id="9607e-162">El codificador H. 264 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer los parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="9607e-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="9607e-163">Admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="9607e-163">It supports the following properties.</span></span>

<span data-ttu-id="9607e-164">Para conocer los requisitos de códec para la certificación del codificador de HCK, consulte la sección sobre el **codificador de hardware certificado** a continuación.</span><span class="sxs-lookup"><span data-stu-id="9607e-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="9607e-165">Las siguientes propiedades se admiten en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9607e-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="9607e-166">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9607e-166">Property</span></span>                                                                              | <span data-ttu-id="9607e-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="9607e-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9607e-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="9607e-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="9607e-169">Establece el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-169">Sets the rate control mode.</span></span> <span data-ttu-id="9607e-170">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9607e-170">See Remarks.</span></span> <span data-ttu-id="9607e-171">El modo predeterminado es la velocidad de bits variable (VBR) sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="9607e-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="9607e-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="9607e-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="9607e-173">Establece el nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-173">Sets the quality level.</span></span> <span data-ttu-id="9607e-174">Esta propiedad se aplica cuando el modo de control de velocidad es VBR basada en la calidad (**eAVEncCommonRateControlMode_Quality**).</span><span class="sxs-lookup"><span data-stu-id="9607e-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="9607e-175">El intervalo válido es de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="9607e-175">The valid range is 1–100.</span></span> <span data-ttu-id="9607e-176">El valor predeterminado es 70.</span><span class="sxs-lookup"><span data-stu-id="9607e-176">The default value is 70.</span></span> <br/> <span data-ttu-id="9607e-177">Para establecer este parámetro, establezca la propiedad antes de llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="9607e-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="9607e-178">Para establecer este parámetro en Windows 7, establezca la propiedad antes de llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="9607e-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="9607e-179">El codificador omite los cambios después de establecer el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="9607e-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="9607e-180">En Windows 8, esta propiedad se puede establecer en cualquier momento durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="9607e-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="9607e-181">Los cambios se aplican a partir del siguiente fotograma de entrada.</span><span class="sxs-lookup"><span data-stu-id="9607e-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="9607e-182">Internamente, el codificador convierte esta propiedad en un valor [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="9607e-183">Las siguientes propiedades requieren Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9607e-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9607e-184">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9607e-184">Property</span></span></th>
<th><span data-ttu-id="9607e-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="9607e-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9607e-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="9607e-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="9607e-187">Establece el modo de codificación adaptable.</span><span class="sxs-lookup"><span data-stu-id="9607e-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="9607e-188">El codificador H. 264 admite los siguientes modos en Windows 8:</span><span class="sxs-lookup"><span data-stu-id="9607e-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="9607e-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="9607e-190">Sin codificación adaptable.</span><span class="sxs-lookup"><span data-stu-id="9607e-190">No adaptive encoding.</span></span> <span data-ttu-id="9607e-191">(Valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="9607e-191">(Default.)</span></span></li>
<li><span data-ttu-id="9607e-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="9607e-193">Cambiar la velocidad de fotogramas de un modo adaptable.</span><span class="sxs-lookup"><span data-stu-id="9607e-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="9607e-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="9607e-195">Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="9607e-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="9607e-196">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="9607e-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="9607e-197">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9607e-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="9607e-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="9607e-199">En el caso de la codificación VBR restringida, especifica la velocidad a la que &quot; se purga el depósito de fugas &quot; , en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9607e-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="9607e-200">Esta propiedad se aplica cuando se <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="9607e-201">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="9607e-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="9607e-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="9607e-203">Establece la velocidad de bits promedio para el flujo de bits codificado, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9607e-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="9607e-204">Esta propiedad se omite si el modo de control de velocidad es <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="9607e-205">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="9607e-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="9607e-206">En los modos CBR y VBR sin restricciones, la velocidad de bits promedio determina el tamaño final del archivo.</span><span class="sxs-lookup"><span data-stu-id="9607e-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="9607e-207">En el modo CBR, la velocidad de bits promedio es también la velocidad a la que los bits comprimidos se purgan del &quot; depósito de fugas. &quot; (para obtener más información, vea <a href="the-leaky-bucket-buffer-model.md">el modelo de búfer de depósitos con fugas</a>).</span><span class="sxs-lookup"><span data-stu-id="9607e-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="9607e-208">En Windows 7, la velocidad de bits promedio se especifica mediante el atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="9607e-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="9607e-209">En Windows 8, puede establecer la velocidad de bits promedio mediante el <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> atributo o la propiedad <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> .</span><span class="sxs-lookup"><span data-stu-id="9607e-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="9607e-210">Si se establecen ambos, CODECAPI_AVEncCommonMeanBitRate invalida.</span><span class="sxs-lookup"><span data-stu-id="9607e-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="9607e-211">En Windows 8, puede establecer la velocidad de bits promedio durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="9607e-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="9607e-212">Si la velocidad de bits cambia, el codificador utiliza la codificación adaptable.</span><span class="sxs-lookup"><span data-stu-id="9607e-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="9607e-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="9607e-214">Establece el equilibrio de calidad/velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="9607e-215">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="9607e-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="9607e-216">0 – 33: baja complejidad</span><span class="sxs-lookup"><span data-stu-id="9607e-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="9607e-217">34 – 66: complejidad media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="9607e-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="9607e-218">67 – 100: alta complejidad</span><span class="sxs-lookup"><span data-stu-id="9607e-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="9607e-219">Este valor afecta al modo en que el codificador realiza varias operaciones de codificación, como la compensación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="9607e-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="9607e-220">En los niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="9607e-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="9607e-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="9607e-222">Habilita o deshabilita CABAC (codificación aritmética binaria adaptable al contexto) para la codificación de entropía H. 264.</span><span class="sxs-lookup"><span data-stu-id="9607e-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="9607e-223">El valor predeterminado es <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="9607e-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="9607e-224">CABAC no se utiliza para el perfil de línea base.</span><span class="sxs-lookup"><span data-stu-id="9607e-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="9607e-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="9607e-226">Establece el valor de <strong>seq_parameter_set_id</strong> en la unidad nal de SPS del fragmentada H. 264.</span><span class="sxs-lookup"><span data-stu-id="9607e-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="9607e-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="9607e-228">Establece el número máximo de fotogramas B consecutivos en el fragmentada de salida.</span><span class="sxs-lookup"><span data-stu-id="9607e-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="9607e-229">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="9607e-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="9607e-230">0: no usar fotogramas B (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="9607e-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="9607e-231">1: Use un marco B.</span><span class="sxs-lookup"><span data-stu-id="9607e-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="9607e-232">2: Use dos fotogramas B.</span><span class="sxs-lookup"><span data-stu-id="9607e-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="9607e-233">Para establecer este parámetro, establezca la propiedad antes de llamar a <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9607e-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="9607e-234">Para el perfil de línea base, el número de fotogramas B siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="9607e-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="9607e-235">El codificador invalidará los valores distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="9607e-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="9607e-236">Para otros perfiles H. 264, si esta propiedad es distinta de cero, el patrón de codificación es IBBPBBP, donde el número máximo de fotogramas B consecutivos es igual que <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span><span class="sxs-lookup"><span data-stu-id="9607e-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="9607e-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="9607e-238">Establece el número de imágenes desde un encabezado GOP hasta el siguiente, incluido el delimitador inicial, pero no el siguiente.</span><span class="sxs-lookup"><span data-stu-id="9607e-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="9607e-239">El intervalo válido es [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="9607e-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="9607e-240">Si el valor es cero, el codificador selecciona el tamaño de GOP.</span><span class="sxs-lookup"><span data-stu-id="9607e-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="9607e-241">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="9607e-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="9607e-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="9607e-243">Establece el número de subprocesos de trabajo que utiliza un codificador.</span><span class="sxs-lookup"><span data-stu-id="9607e-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="9607e-244">El intervalo válido es de 0 a 16.</span><span class="sxs-lookup"><span data-stu-id="9607e-244">The valid range is 0–16.</span></span> <span data-ttu-id="9607e-245">Si el valor es cero, el codificador selecciona el número de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9607e-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="9607e-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="9607e-247">Indica el tipo de contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9607e-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="9607e-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="9607e-249">Intervalo válido: 16 – 51.</span><span class="sxs-lookup"><span data-stu-id="9607e-249">Valid range: 16–51.</span></span> <span data-ttu-id="9607e-250">El valor predeterminado es 24.</span><span class="sxs-lookup"><span data-stu-id="9607e-250">The default value is 24.</span></span> <br/> <span data-ttu-id="9607e-251">Esta propiedad se aplica cuando se <strong>eAVEncCommonRateControlMode_Quality</strong>el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="9607e-252">Esta propiedad configura la misma configuración de codificación que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9607e-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="9607e-253">Sin embargo, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite que la aplicación especifique el valor de QP directamente.</span><span class="sxs-lookup"><span data-stu-id="9607e-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="9607e-254">Si se establecen ambas propiedades, AVEncVideoEncodeQP invalida.</span><span class="sxs-lookup"><span data-stu-id="9607e-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="9607e-255">El valor predeterminado de 24 corresponde al valor predeterminado de 70 para la configuración de <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9607e-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="9607e-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="9607e-257">Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="9607e-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9607e-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="9607e-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="9607e-259">Intervalo válido: 0 – 51.</span><span class="sxs-lookup"><span data-stu-id="9607e-259">Valid range: 0–51.</span></span> <span data-ttu-id="9607e-260">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="9607e-260">The default value is 0.</span></span> <br/> <span data-ttu-id="9607e-261">Esta propiedad se aplica a todos los modos de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="9607e-262">El codificador no debe producir un valor de QP inferior a lo especificado por la propiedad <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .</span><span class="sxs-lookup"><span data-stu-id="9607e-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9607e-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="9607e-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="9607e-264">Habilita o deshabilita el modo de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="9607e-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="9607e-265">Vea &quot; multithreading &quot; en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9607e-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9607e-266">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9607e-266">Remarks</span></span>

<span data-ttu-id="9607e-267">El codificador admite los siguientes modos de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="9607e-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="9607e-268">Mode</span><span class="sxs-lookup"><span data-stu-id="9607e-268">Mode</span></span>                                  | <span data-ttu-id="9607e-269">Constante</span><span class="sxs-lookup"><span data-stu-id="9607e-269">Constant</span></span>                                            | <span data-ttu-id="9607e-270">Descripción</span><span class="sxs-lookup"><span data-stu-id="9607e-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9607e-271">Velocidad de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="9607e-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="9607e-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="9607e-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="9607e-273">El codificador intenta alcanzar una velocidad de bits constante, mediante un modelo de "depósito de fugas".</span><span class="sxs-lookup"><span data-stu-id="9607e-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="9607e-274">La velocidad de bits de destino la proporciona la propiedad [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="9607e-275">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9607e-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="9607e-276">Velocidad de bits variable restringida (VBR)</span><span class="sxs-lookup"><span data-stu-id="9607e-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="9607e-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="9607e-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="9607e-278">El codificador usa un modelo de "depósito de fugas" con una velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="9607e-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="9607e-279">La tasa de purga del depósito de fugas viene determinada por la propiedad [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="9607e-280">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9607e-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="9607e-281">Velocidad de bits variable basada en la calidad (VBR)</span><span class="sxs-lookup"><span data-stu-id="9607e-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="9607e-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="9607e-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="9607e-283">El codificador intenta alcanzar un nivel de calidad constante, proporcionado por la propiedad [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="9607e-284">VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="9607e-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="9607e-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="9607e-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="9607e-286">El codificador intenta lograr la velocidad de bits de destino proporcionada por el [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) atributo en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="9607e-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="9607e-287">Este es el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9607e-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="9607e-288">Los modos CBR y VBR restringida requieren Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9607e-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="9607e-289">En Windows 8, el codificador establece los siguientes atributos en los ejemplos de salida:</span><span class="sxs-lookup"><span data-stu-id="9607e-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="9607e-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="9607e-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="9607e-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="9607e-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="9607e-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="9607e-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="9607e-293">Una versión anterior de la documentación indicó incorrectamente que el codificador es compatible con Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="9607e-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="9607e-294">Subprocesamiento múltiple</span><span class="sxs-lookup"><span data-stu-id="9607e-294">Multithreading</span></span>

<span data-ttu-id="9607e-295">En Windows 8, el codificador admite dos modos de codificación:</span><span class="sxs-lookup"><span data-stu-id="9607e-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="9607e-296">**Codificación del segmento.**</span><span class="sxs-lookup"><span data-stu-id="9607e-296">**Slice encoding.**</span></span> <span data-ttu-id="9607e-297">En este modo, los segmentos se codifican en paralelo.</span><span class="sxs-lookup"><span data-stu-id="9607e-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="9607e-298">Cada segmento se codifica en un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="9607e-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="9607e-299">Este modo tiene una latencia baja, porque una sola imagen está codificada en paralelo.</span><span class="sxs-lookup"><span data-stu-id="9607e-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="9607e-300">Sin embargo, este enfoque no escala a medida que aumenta el número de núcleos, ya que el número de segmentos está limitado por el número de filas de adaptativo macrobloque en la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="9607e-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="9607e-301">**Codificación de varios marcos.**</span><span class="sxs-lookup"><span data-stu-id="9607e-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="9607e-302">En este modo, el codificador acepta varios fotogramas de entrada y los codifica en paralelo.</span><span class="sxs-lookup"><span data-stu-id="9607e-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="9607e-303">Este modo se escala mejor en un entorno de varios núcleos, pero introduce más latencia.</span><span class="sxs-lookup"><span data-stu-id="9607e-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="9607e-304">El codificador tiene como valor predeterminado la codificación de segmentos, para minimizar la latencia.</span><span class="sxs-lookup"><span data-stu-id="9607e-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="9607e-305">Para habilitar la codificación de varios marcos, establezca la propiedad [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) en **VARIANT_FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9607e-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="9607e-306">Para establecer el número de subprocesos de trabajo utilizados por el codificador, establezca la propiedad [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="9607e-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="9607e-307">En Windows 7, el codificador siempre usa la codificación de sectores.</span><span class="sxs-lookup"><span data-stu-id="9607e-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="9607e-308">Codificador de hardware certificado</span><span class="sxs-lookup"><span data-stu-id="9607e-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="9607e-309">Si hay un codificador de hardware certificado, se usará generalmente en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados.</span><span class="sxs-lookup"><span data-stu-id="9607e-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="9607e-310">Los codificadores certificados son necesarios para admitir un conjunto determinado de propiedades de **ICodecAPI** y, opcionalmente, admiten otro conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9607e-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="9607e-311">El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.</span><span class="sxs-lookup"><span data-stu-id="9607e-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="9607e-312">El siguiente es el conjunto de propiedades **ICodecAPI** necesarias y opcionales para los codificadores para pasar la certificación del codificador HCK.</span><span class="sxs-lookup"><span data-stu-id="9607e-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="9607e-313">Se requieren las siguientes propiedades **ICodecAPI** de Windows 8 y Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="9607e-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="9607e-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="9607e-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="9607e-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="9607e-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="9607e-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="9607e-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="9607e-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="9607e-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="9607e-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="9607e-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="9607e-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="9607e-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="9607e-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="9607e-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="9607e-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="9607e-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="9607e-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="9607e-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="9607e-323">Las siguientes Windows 8.1 propiedades de **ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.</span><span class="sxs-lookup"><span data-stu-id="9607e-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="9607e-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="9607e-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="9607e-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="9607e-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="9607e-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="9607e-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="9607e-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="9607e-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="9607e-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="9607e-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="9607e-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="9607e-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="9607e-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="9607e-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="9607e-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="9607e-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="9607e-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="9607e-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="9607e-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="9607e-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="9607e-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="9607e-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="9607e-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinámico)</span><span class="sxs-lookup"><span data-stu-id="9607e-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="9607e-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="9607e-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="9607e-337">Las siguientes propiedades de Windows 8 y Windows 8.1 **ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.</span><span class="sxs-lookup"><span data-stu-id="9607e-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="9607e-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (estático)</span><span class="sxs-lookup"><span data-stu-id="9607e-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="9607e-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="9607e-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="9607e-340">Las siguientes propiedades de **ICodecAPI** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="9607e-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="9607e-341">No se prueban en HCK.</span><span class="sxs-lookup"><span data-stu-id="9607e-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="9607e-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="9607e-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="9607e-343">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9607e-343">Requirements</span></span>



| <span data-ttu-id="9607e-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="9607e-344">Requirement</span></span> | <span data-ttu-id="9607e-345">Value</span><span class="sxs-lookup"><span data-stu-id="9607e-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9607e-346">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9607e-346">Minimum supported client</span></span><br/> | <span data-ttu-id="9607e-347">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9607e-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9607e-348">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9607e-348">Minimum supported server</span></span><br/> | <span data-ttu-id="9607e-349">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9607e-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9607e-350">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9607e-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9607e-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9607e-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9607e-352">Vea también</span><span class="sxs-lookup"><span data-stu-id="9607e-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9607e-353">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="9607e-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="9607e-354">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9607e-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9607e-355">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9607e-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9607e-356">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="9607e-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
