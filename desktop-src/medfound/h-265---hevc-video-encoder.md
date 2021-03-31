---
description: El codificador de vídeo H. 265 Media Foundation es una transformación de Media Foundation que admite la codificación de contenido en el formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC de vídeo codificador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001407"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="493e0-103">H. 265/HEVC de vídeo codificador</span><span class="sxs-lookup"><span data-stu-id="493e0-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="493e0-104">El codificador de vídeo H. 265 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la codificación de contenido en el formato H. 265/HEVC.</span><span class="sxs-lookup"><span data-stu-id="493e0-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="493e0-105">El codificador admite los siguientes perfiles:</span><span class="sxs-lookup"><span data-stu-id="493e0-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="493e0-106">Perfil Main</span><span class="sxs-lookup"><span data-stu-id="493e0-106">Main Profile</span></span>

<span data-ttu-id="493e0-107">El codificador de vídeo H. 265 expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="493e0-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="493e0-108">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="493e0-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="493e0-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="493e0-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="493e0-110">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="493e0-110">Input Types</span></span>

<span data-ttu-id="493e0-111">El tipo de medio de entrada debe tener uno de los siguientes subtipos:</span><span class="sxs-lookup"><span data-stu-id="493e0-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="493e0-112">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="493e0-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="493e0-113">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="493e0-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="493e0-114">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="493e0-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="493e0-115">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="493e0-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="493e0-116">Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="493e0-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="493e0-117">El tipo de salida debe establecerse antes que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="493e0-117">The output type must be set before the input type.</span></span> <span data-ttu-id="493e0-118">Hasta que se establezca el tipo de salida, el método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificador devuelve el **tipo de \_ transformación MF E \_ \_ \_ no \_ establecido**.</span><span class="sxs-lookup"><span data-stu-id="493e0-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="493e0-119">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="493e0-119">Output Types</span></span>

<span data-ttu-id="493e0-120">El codificador admite un solo subtipo de salida:</span><span class="sxs-lookup"><span data-stu-id="493e0-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="493e0-121">**MFVideoFormat \_ H265**</span><span class="sxs-lookup"><span data-stu-id="493e0-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="493e0-122">Establezca los siguientes atributos en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="493e0-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="493e0-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="493e0-123">Attribute</span></span></th>
<th><span data-ttu-id="493e0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="493e0-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="493e0-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-126">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="493e0-126">Major type.</span></span> <span data-ttu-id="493e0-127">Debe ser <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="493e0-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-129">Subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="493e0-129">Video subtype.</span></span> <span data-ttu-id="493e0-130">Debe ser <strong>MFVideoFormat_HEVC</strong>.</span><span class="sxs-lookup"><span data-stu-id="493e0-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-132">Velocidad media de bits codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="493e0-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="493e0-133">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="493e0-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-135">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="493e0-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-137">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="493e0-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="493e0-139">Modo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="493e0-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="493e0-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="493e0-141">Perfil de codificación H. 265.</span><span class="sxs-lookup"><span data-stu-id="493e0-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="493e0-142">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="493e0-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="493e0-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="493e0-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="493e0-145">Especifica el nivel del vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="493e0-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="493e0-146">Para obtener más información acerca de las restricciones de perfil y de nivel, consulte el anexo a de ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="493e0-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="493e0-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="493e0-148">Optional.</span></span> <span data-ttu-id="493e0-149">Especifica la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="493e0-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="493e0-150">El valor predeterminado es 1:1.</span><span class="sxs-lookup"><span data-stu-id="493e0-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="493e0-151">Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando el atributo de [**\_ encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="493e0-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="493e0-152">Este atributo contiene el encabezado de secuencia.</span><span class="sxs-lookup"><span data-stu-id="493e0-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="493e0-153">Métodos de IMFTransform admitidos</span><span class="sxs-lookup"><span data-stu-id="493e0-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="493e0-154">Los siguientes métodos de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) son compatibles con el codificador H. 265/HEVC:</span><span class="sxs-lookup"><span data-stu-id="493e0-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="493e0-155">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="493e0-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="493e0-156">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="493e0-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="493e0-157">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="493e0-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="493e0-158">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="493e0-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="493e0-159">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="493e0-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="493e0-160">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="493e0-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="493e0-161">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="493e0-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="493e0-162">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="493e0-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="493e0-163">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="493e0-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="493e0-164">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="493e0-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="493e0-165">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="493e0-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="493e0-166">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="493e0-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="493e0-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="493e0-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="493e0-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="493e0-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="493e0-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="493e0-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="493e0-170">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="493e0-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="493e0-171">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="493e0-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="493e0-172">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="493e0-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="493e0-173">Todos los demás métodos de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devolverán el error E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="493e0-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="493e0-174">Métodos de ICodecAPI admitidos</span><span class="sxs-lookup"><span data-stu-id="493e0-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="493e0-175">Los siguientes métodos de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) son compatibles con el codificador H. 265/HEVC:</span><span class="sxs-lookup"><span data-stu-id="493e0-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="493e0-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="493e0-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="493e0-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="493e0-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="493e0-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="493e0-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="493e0-179">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="493e0-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="493e0-180">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="493e0-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="493e0-181">Todos los demás métodos de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) devolverán el error E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="493e0-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="493e0-182">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="493e0-182">Codec Properties</span></span>

<span data-ttu-id="493e0-183">El codificador H. 265 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer los parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="493e0-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="493e0-184">Admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="493e0-184">It supports the following properties.</span></span>

<span data-ttu-id="493e0-185">Para conocer los requisitos de códec para la certificación del codificador de HCK, consulte la sección sobre el **codificador de hardware certificado** a continuación.</span><span class="sxs-lookup"><span data-stu-id="493e0-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="493e0-186">Propiedad</span><span class="sxs-lookup"><span data-stu-id="493e0-186">Property</span></span></th>
<th><span data-ttu-id="493e0-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="493e0-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="493e0-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="493e0-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="493e0-189">Establece el modo de control de velocidad.</span><span class="sxs-lookup"><span data-stu-id="493e0-189">Sets the rate control mode.</span></span> <span data-ttu-id="493e0-190">Los modos admitidos son:</span><span class="sxs-lookup"><span data-stu-id="493e0-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="493e0-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="493e0-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="493e0-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="493e0-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="493e0-193">Si se especifican otros modos, se usará el control de velocidad de <strong>eAVEncCommonRateControlMode_CBR</strong> .</span><span class="sxs-lookup"><span data-stu-id="493e0-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="493e0-194">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="493e0-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="493e0-196">Establece la velocidad de bits promedio para el flujo de bits codificado, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="493e0-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="493e0-197">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="493e0-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="493e0-198">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="493e0-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="493e0-200">Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="493e0-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="493e0-201">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="493e0-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="493e0-202">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="493e0-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="493e0-204">Establece la velocidad de bits máxima para los modos de control de velocidad que permiten una velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="493e0-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="493e0-205">El intervalo válido es [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="493e0-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="493e0-206">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="493e0-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="493e0-208">Establece el número de imágenes desde un encabezado GOP hasta el siguiente, incluido el delimitador inicial, pero no el siguiente.</span><span class="sxs-lookup"><span data-stu-id="493e0-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="493e0-209">El intervalo válido es [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="493e0-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="493e0-210">Si el valor es cero, el codificador selecciona el tamaño de GOP.</span><span class="sxs-lookup"><span data-stu-id="493e0-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="493e0-211">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="493e0-211">The default value is zero.</span></span> <br/> <span data-ttu-id="493e0-212">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="493e0-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="493e0-214">Habilita o deshabilita el modo de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="493e0-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="493e0-215">Se trata de un valor de VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="493e0-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="493e0-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="493e0-217">Establece el equilibrio de calidad/velocidad.</span><span class="sxs-lookup"><span data-stu-id="493e0-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="493e0-218">Este valor afecta al modo en que el codificador realiza varias operaciones de codificación, como la compensación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="493e0-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="493e0-219">En los niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="493e0-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="493e0-220">El intervalo válido es de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="493e0-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="493e0-221">Internamente, este valor se asigna a un conjunto más pequeño de niveles de calidad/velocidad que admite el codificador.</span><span class="sxs-lookup"><span data-stu-id="493e0-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="493e0-222">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="493e0-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="493e0-224">Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="493e0-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="493e0-225">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="493e0-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="493e0-227">Cuando se establece esta propiedad, el codificador usará el QP especificado para codificar el fotograma siguiente y todos los fotogramas posteriores hasta que se especifique un nuevo QP.</span><span class="sxs-lookup"><span data-stu-id="493e0-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="493e0-228">Intervalo válido: 0 – 51, ambos incluidos</span><span class="sxs-lookup"><span data-stu-id="493e0-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="493e0-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="493e0-230">Esta propiedad establecerá un límite en el valor de QP mínimo que el codificador puede utilizar durante RateControl CBR.</span><span class="sxs-lookup"><span data-stu-id="493e0-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="493e0-231">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="493e0-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="493e0-233">Esta propiedad establecerá un límite en el valor de QP máximo que el codificador puede utilizar durante RateControl CBR.</span><span class="sxs-lookup"><span data-stu-id="493e0-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="493e0-234">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493e0-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="493e0-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="493e0-236">Establece si el contenido está en pantalla completa, en lugar de en el contenido de pantalla que podría tener una ventana de vídeo más pequeña o no tener ningún vídeo.</span><span class="sxs-lookup"><span data-stu-id="493e0-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="493e0-237">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493e0-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="493e0-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="493e0-239">Establece el número de subprocesos utilizados para realizar la operación de compresión.</span><span class="sxs-lookup"><span data-stu-id="493e0-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="493e0-240">El codificador dividirá el marco en mosaicos de forma que el número de subprocesos sea igual al número de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="493e0-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="493e0-241">El número de procesadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="493e0-241">The number of logical processors.</span></span> <span data-ttu-id="493e0-242">El número de subprocesos debe ser menor o igual que el número de procesadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="493e0-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="493e0-243">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="493e0-243">The size of the frame.</span></span> <span data-ttu-id="493e0-244">El tamaño de un icono debe ser mayor o igual que 265x64 píxeles.</span><span class="sxs-lookup"><span data-stu-id="493e0-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="493e0-245">Paridad.</span><span class="sxs-lookup"><span data-stu-id="493e0-245">Parity.</span></span> <span data-ttu-id="493e0-246">El número de subprocesos debe ser un valor par.</span><span class="sxs-lookup"><span data-stu-id="493e0-246">The number of threads must be an even value.</span></span> <span data-ttu-id="493e0-247">Si el valor especificado es impar, se utilizará el siguiente valor par inferior.</span><span class="sxs-lookup"><span data-stu-id="493e0-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="493e0-248">Se trata de un valor de VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="493e0-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="493e0-249">Codificador de hardware certificado</span><span class="sxs-lookup"><span data-stu-id="493e0-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="493e0-250">Si hay un codificador de hardware certificado, se usará generalmente en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados.</span><span class="sxs-lookup"><span data-stu-id="493e0-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="493e0-251">Los codificadores certificados son necesarios para admitir un conjunto determinado de propiedades de **ICodecAPI** y, opcionalmente, admiten otro conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="493e0-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="493e0-252">El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.</span><span class="sxs-lookup"><span data-stu-id="493e0-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="493e0-253">El siguiente es el conjunto de propiedades **ICodecAPI** necesarias y opcionales para los codificadores para pasar la certificación del codificador HCK.</span><span class="sxs-lookup"><span data-stu-id="493e0-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="493e0-254">CODECAPI \_ AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="493e0-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="493e0-255">CODECAPI \_ AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="493e0-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="493e0-256">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="493e0-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="493e0-257">CODECAPI \_ AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="493e0-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="493e0-258">CODECAPI \_ AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="493e0-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="493e0-259">CODECAPI \_ AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="493e0-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="493e0-260">CODECAPI \_ AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="493e0-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="493e0-261">Requisitos</span><span class="sxs-lookup"><span data-stu-id="493e0-261">Requirements</span></span>



| <span data-ttu-id="493e0-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="493e0-262">Requirement</span></span> | <span data-ttu-id="493e0-263">Value</span><span class="sxs-lookup"><span data-stu-id="493e0-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="493e0-264">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="493e0-264">Minimum supported client</span></span><br/> | <span data-ttu-id="493e0-265">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="493e0-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="493e0-266">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="493e0-266">Minimum supported server</span></span><br/> | <span data-ttu-id="493e0-267">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="493e0-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="493e0-268">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="493e0-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493e0-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493e0-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493e0-270">Vea también</span><span class="sxs-lookup"><span data-stu-id="493e0-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493e0-271">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="493e0-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
