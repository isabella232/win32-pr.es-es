---
description: El descodificador de vídeo MPEG-2 es una transformación Media Foundation que descodifica vídeo MPEG-1 y MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Descodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543894"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="cb566-103">Descodificador de vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="cb566-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="cb566-104">El descodificador de vídeo MPEG-2 es una [transformación Media Foundation](media-foundation-transforms.md) que DESCODIFICA vídeo MPEG-1 y MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="cb566-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="cb566-105">El descodificador admite el vídeo MPEG-2 simple y el perfil principal (H. 262, ISO/IEC 13818-2) y MPEG-1 (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="cb566-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="cb566-106">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="cb566-106">Input Types</span></span>

<span data-ttu-id="cb566-107">El descodificador admite los siguientes tipos de medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb566-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="cb566-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="cb566-108">Attribute</span></span>                                                 | <span data-ttu-id="cb566-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb566-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="cb566-110">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cb566-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="cb566-111">**Vídeo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="cb566-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="cb566-112">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="cb566-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="cb566-113">**MFVideoFormat \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="cb566-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="cb566-114">**MFVideoFormat \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="cb566-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="cb566-115">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="cb566-115">Output Types</span></span>

<span data-ttu-id="cb566-116">El descodificador admite los siguientes tipos de salida.</span><span class="sxs-lookup"><span data-stu-id="cb566-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="cb566-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="cb566-117">Attribute</span></span>                                                 | <span data-ttu-id="cb566-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb566-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb566-119">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cb566-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="cb566-120">**Vídeo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="cb566-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="cb566-121">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="cb566-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="cb566-122">**MFVideoFormat \_ i420**</span><span class="sxs-lookup"><span data-stu-id="cb566-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="cb566-123">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="cb566-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="cb566-124">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="cb566-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="cb566-125">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="cb566-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="cb566-126">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="cb566-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb566-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb566-127">Remarks</span></span>

<span data-ttu-id="cb566-128">El descodificador de vídeo MPEG-2 expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="cb566-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="cb566-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cb566-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="cb566-130">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="cb566-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="cb566-131">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="cb566-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="cb566-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="cb566-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="cb566-133">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="cb566-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="cb566-134">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="cb566-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="cb566-135">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="cb566-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="cb566-136">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="cb566-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="cb566-137">La entrada para el descodificador debe ser una secuencia elemental.</span><span class="sxs-lookup"><span data-stu-id="cb566-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="cb566-138">La resolución máxima admitida es 1920 × 1088 píxeles.</span><span class="sxs-lookup"><span data-stu-id="cb566-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="cb566-139">El descodificador es compatible con DirectX video Acceleration (DXVA) mediante Microsoft Direct3D 9 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cb566-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="cb566-140">Modos de descodificación especiales</span><span class="sxs-lookup"><span data-stu-id="cb566-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="cb566-141">**Modo de baja latencia.**</span><span class="sxs-lookup"><span data-stu-id="cb566-141">**Low latency mode.**</span></span> <span data-ttu-id="cb566-142">Este modo es adecuado para escenarios como las comunicaciones en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="cb566-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="cb566-143">Reduce la latencia de inicio, por lo que el descodificador genera el primer ejemplo de salida antes.</span><span class="sxs-lookup"><span data-stu-id="cb566-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="cb566-144">Sin embargo, el descodificador almacena menos muestras en este modo, lo que puede provocar problemas, porque el descodificador no descodifica tantas tramas de antemano.</span><span class="sxs-lookup"><span data-stu-id="cb566-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="cb566-145">Para habilitar el modo de baja latencia, establezca el atributo [ \_ AVLowLatencyMode de CODECAPI](codecapi-avlowlatencymode.md) .</span><span class="sxs-lookup"><span data-stu-id="cb566-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="cb566-146">**Invoca.**</span><span class="sxs-lookup"><span data-stu-id="cb566-146">**Seeking.**</span></span> <span data-ttu-id="cb566-147">Para una búsqueda precisa, llame al método [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) .</span><span class="sxs-lookup"><span data-stu-id="cb566-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="cb566-148">Cuando se llama a este método, el descodificador solo genera fotogramas que se encuentran dentro del intervalo de marcas de tiempo especificado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="cb566-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="cb566-149">**Modo de generación de miniaturas**.</span><span class="sxs-lookup"><span data-stu-id="cb566-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="cb566-150">Este modo está diseñado para la generación rápida de imágenes en miniatura.</span><span class="sxs-lookup"><span data-stu-id="cb566-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="cb566-151">En este modo, el descodificador descodifica inicialmente solo I fotogramas.</span><span class="sxs-lookup"><span data-stu-id="cb566-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="cb566-152">Si no se encuentra ningún fotograma I dentro de un número determinado de fotogramas, el descodificador inicia la descodificación de los fotogramas P y genera las tramas que no son I en un intervalo fijo (uno por *N* imágenes) hasta que se alcanza un fotograma I.</span><span class="sxs-lookup"><span data-stu-id="cb566-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="cb566-153">Para habilitar el modo de generación de miniaturas, establezca la propiedad [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="cb566-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="cb566-154">**Juegue.**</span><span class="sxs-lookup"><span data-stu-id="cb566-154">**Trick play.**</span></span> <span data-ttu-id="cb566-155">El descodificador puede descodificar a velocidades más rápido que en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="cb566-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="cb566-156">Con una velocidad de reproducción mayor, el descodificador cambiará a descodificar solo I fotogramas.</span><span class="sxs-lookup"><span data-stu-id="cb566-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="cb566-157">Para la reproducción inversa, solo se descodifican las tramas I.</span><span class="sxs-lookup"><span data-stu-id="cb566-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="cb566-158">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="cb566-158">Codec Properties</span></span>

<span data-ttu-id="cb566-159">El descodificador admite las siguientes propiedades a través del método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="cb566-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="cb566-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb566-160">Property</span></span>                                                                                                      | <span data-ttu-id="cb566-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb566-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb566-162">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="cb566-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="cb566-163">Habilita o deshabilita el modo de generación de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="cb566-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="cb566-164">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="cb566-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="cb566-165">Habilita o deshabilita la descodificación acelerada de hardware.</span><span class="sxs-lookup"><span data-stu-id="cb566-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="cb566-166">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="cb566-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="cb566-167">Habilita o deshabilita el modo de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="cb566-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="cb566-168">el \_ DEScodificador \_ de MFT expone \_ \_ tipos \_ de salida en \_ \_ orden nativo</span><span class="sxs-lookup"><span data-stu-id="cb566-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="cb566-169">Especifica si el descodificador expone los tipos de salida adecuados para la transcodificación antes de otros formatos.</span><span class="sxs-lookup"><span data-stu-id="cb566-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="cb566-170">De estas propiedades, también se pueden establecer las siguientes opciones a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="cb566-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="cb566-171">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="cb566-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="cb566-172">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="cb566-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="cb566-173">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="cb566-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="cb566-174">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="cb566-174">Limitations</span></span>

-   <span data-ttu-id="cb566-175">El descodificador no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="cb566-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="cb566-176">El descodificador no admite el descifrado de CSS ni la reproducción de DVDs cifrados.</span><span class="sxs-lookup"><span data-stu-id="cb566-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb566-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb566-177">Requirements</span></span>



| <span data-ttu-id="cb566-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb566-178">Requirement</span></span> | <span data-ttu-id="cb566-179">Value</span><span class="sxs-lookup"><span data-stu-id="cb566-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb566-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb566-180">Minimum supported client</span></span><br/> | <span data-ttu-id="cb566-181">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb566-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb566-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb566-182">Minimum supported server</span></span><br/> | <span data-ttu-id="cb566-183">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb566-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cb566-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb566-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb566-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb566-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb566-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb566-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb566-187">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="cb566-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
