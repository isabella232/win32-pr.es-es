---
description: El descodificador de vídeo H. 265 Media Foundation es una transformación de Media Foundation que admite la descodificación del contenido H. 265/HEVC en el formato del Anexo B y se puede usar en la reproducción de archivos MP4 y M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Descodificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543622"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="9d734-103">Descodificador de vídeo H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="9d734-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="9d734-104">El descodificador de vídeo H. 265 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la descodificación del contenido H. 265/HEVC en el formato del Anexo B y se puede usar en la reproducción de archivos MP4 y M2TS.</span><span class="sxs-lookup"><span data-stu-id="9d734-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="9d734-105">El descodificador de vídeo H. 265 expone las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="9d734-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="9d734-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)</span><span class="sxs-lookup"><span data-stu-id="9d734-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="9d734-107">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="9d734-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="9d734-108">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="9d734-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="9d734-109">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="9d734-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="9d734-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="9d734-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="9d734-111">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="9d734-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="9d734-112">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="9d734-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="9d734-113">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="9d734-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="9d734-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="9d734-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="9d734-115">Para crear una instancia del descodificador, llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="9d734-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="9d734-116">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="9d734-116">Input Types</span></span>

<span data-ttu-id="9d734-117">El tipo de entrada debe contener al menos los dos atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9d734-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="9d734-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="9d734-118">Attribute</span></span>                                                 | <span data-ttu-id="9d734-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d734-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d734-120">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="9d734-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="9d734-121">**Vídeo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="9d734-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="9d734-122">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="9d734-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="9d734-123">[MFVideoFormat \_ HEVC](video-subtype-guids.md) o MFVideoFormat \_ HEVC \_ es</span><span class="sxs-lookup"><span data-stu-id="9d734-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="9d734-124">El primer subtipo de medio, MFVideoFormat \_ HEVC, indica que los ejemplos multimedia llevan H. 265 fragmentada con códigos de inicio y que el flujo tiene SP/PPS entrelazado.</span><span class="sxs-lookup"><span data-stu-id="9d734-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="9d734-125">Supone un fotograma por muestra.</span><span class="sxs-lookup"><span data-stu-id="9d734-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="9d734-126">El subtipo de medio MFVideoFormat \_ HEVC \_ es para indicar que los ejemplos de medios transportan la elemental H. 265 fragmentada, donde cada ejemplo puede contener una imagen parcial, varias imágenes, algunas imágenes más una imagen parcial.</span><span class="sxs-lookup"><span data-stu-id="9d734-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="9d734-127">Los tipos de medios de entrada no pueden cambiar dinámicamente entre dos tipos.</span><span class="sxs-lookup"><span data-stu-id="9d734-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="9d734-128">El descodificador puede detectar cambios en el formato de salida en curso en función de la sintaxis de secuencia elemental (relación de aspecto, dimensión, marcas entrelazadas e información de base de datos) y desencadenar los cambios de tipo de medio de salida correspondientes.</span><span class="sxs-lookup"><span data-stu-id="9d734-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="9d734-129">En el caso del tipo de medio de entrada, el descodificador espera que el origen establezca el perfil correcto.</span><span class="sxs-lookup"><span data-stu-id="9d734-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="9d734-130">Por ejemplo, si el contenido va a ser 10 bits, el tipo de medio de entrada debe especificar el perfil como Main10.</span><span class="sxs-lookup"><span data-stu-id="9d734-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="9d734-131">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="9d734-131">Output Types</span></span>

<span data-ttu-id="9d734-132">El descodificador admite los siguientes subtipos de salida:</span><span class="sxs-lookup"><span data-stu-id="9d734-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="9d734-133">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="9d734-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="9d734-134">**MFVideoFormat \_ P010**</span><span class="sxs-lookup"><span data-stu-id="9d734-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="9d734-135">Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9d734-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="9d734-136">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="9d734-136">Transform Attributes</span></span>

<span data-ttu-id="9d734-137">El descodificador H. 265 implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="9d734-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="9d734-138">Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d734-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="9d734-139">Atributo</span><span class="sxs-lookup"><span data-stu-id="9d734-139">Attribute</span></span>                                                                                       | <span data-ttu-id="9d734-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d734-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d734-141">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="9d734-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="9d734-142">Habilita o deshabilita el modo de descodificación de latencia baja.</span><span class="sxs-lookup"><span data-stu-id="9d734-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="9d734-143">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="9d734-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="9d734-144">Establece el número de subprocesos de trabajo utilizados por el descodificador.</span><span class="sxs-lookup"><span data-stu-id="9d734-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="9d734-145">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="9d734-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="9d734-146">Habilita o deshabilita el modo de generación de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="9d734-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="9d734-147">\_conjunto de \_ longitud MF Nalu \_</span><span class="sxs-lookup"><span data-stu-id="9d734-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="9d734-148">Indica que la información de longitud de NALU se enviará como un BLOB con cada ejemplo H. 265 comprimido.</span><span class="sxs-lookup"><span data-stu-id="9d734-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="9d734-149">\_información de \_ longitud de Nalu MF \_</span><span class="sxs-lookup"><span data-stu-id="9d734-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="9d734-150">Indica las longitudes de NALUs en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9d734-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="9d734-151">Se trata de un BLOB MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 265.</span><span class="sxs-lookup"><span data-stu-id="9d734-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="9d734-152">recuento de \_ \_ ejemplo de salida mínima de SA de \_ \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="9d734-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="9d734-153">Especifica el número máximo de ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="9d734-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="9d734-154">El descodificador H. 265 admite la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="9d734-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="9d734-155">Esta interfaz proporciona una API alternativate para configurar las siguientes propiedades de códec.</span><span class="sxs-lookup"><span data-stu-id="9d734-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="9d734-156">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="9d734-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="9d734-157">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="9d734-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="9d734-158">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="9d734-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="9d734-159">Restricciones de formato</span><span class="sxs-lookup"><span data-stu-id="9d734-159">Format Constraints</span></span>

<span data-ttu-id="9d734-160">El descodificador admite los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="9d734-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="9d734-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d734-161">Requirement</span></span> | <span data-ttu-id="9d734-162">Value</span><span class="sxs-lookup"><span data-stu-id="9d734-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d734-163">Perfiles/niveles</span><span class="sxs-lookup"><span data-stu-id="9d734-163">Profiles/Levels</span></span>    | <span data-ttu-id="9d734-164">Perfiles principal, principal y de Main10</span><span class="sxs-lookup"><span data-stu-id="9d734-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="9d734-165">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="9d734-165">Chroma Formats</span></span>     | <span data-ttu-id="9d734-166">croma 4:2:0</span><span class="sxs-lookup"><span data-stu-id="9d734-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9d734-167">Resolución mínima</span><span class="sxs-lookup"><span data-stu-id="9d734-167">Minimum Resolution</span></span> | <span data-ttu-id="9d734-168">48 × 48 píxeles</span><span class="sxs-lookup"><span data-stu-id="9d734-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d734-169">Resolución máxima</span><span class="sxs-lookup"><span data-stu-id="9d734-169">Maximum Resolution</span></span> | <span data-ttu-id="9d734-170">4096 × 2304 píxeles</span><span class="sxs-lookup"><span data-stu-id="9d734-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="9d734-171">La resolución máxima garantizada para la aceleración de DXVA es 1920 × 1088 píxeles; con resoluciones más altas, la descodificación se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, la descodificación se realiza con el software.</span><span class="sxs-lookup"><span data-stu-id="9d734-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="9d734-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="9d734-172">DXVA</span></span>               | <span data-ttu-id="9d734-173">El descodificador admite DX11 y DX12 DXVA, pero no la versión 2 de DXVA o la versión 1 de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9d734-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="9d734-174">Los datos de entrada deben ajustarse al Anexo B de ITU-T H. 265 \| ISO/IEC 23008-2.</span><span class="sxs-lookup"><span data-stu-id="9d734-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="9d734-175">Los datos deben incluir los códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="9d734-175">The data must include the start codes.</span></span> <span data-ttu-id="9d734-176">El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) y un conjunto de parámetros de imagen (PPS) válidos en el flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="9d734-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d734-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d734-177">Requirements</span></span>



| <span data-ttu-id="9d734-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d734-178">Requirement</span></span> | <span data-ttu-id="9d734-179">Value</span><span class="sxs-lookup"><span data-stu-id="9d734-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d734-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d734-180">Minimum supported client</span></span><br/> | <span data-ttu-id="9d734-181">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d734-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9d734-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d734-182">Minimum supported server</span></span><br/> | <span data-ttu-id="9d734-183">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9d734-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9d734-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d734-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d734-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d734-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d734-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d734-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d734-187">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="9d734-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
