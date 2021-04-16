---
description: La MFT del procesador de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la conversión de ColorSpace, el cambio de tamaño de vídeo, el desentrelazado, la conversión de velocidad de fotogramas, la rotación, el recorte, el espacio de la izquierda y la derecha espacial y la creación de reflejo.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT del procesador de vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718975"
---
# <a name="video-processor-mft"></a><span data-ttu-id="d1afe-103">MFT del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="d1afe-103">Video Processor MFT</span></span>

<span data-ttu-id="d1afe-104">La MFT del procesador de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la conversión de ColorSpace, el cambio de tamaño de vídeo, el desentrelazado, la conversión de velocidad de fotogramas, la rotación, el recorte, el espacio de la izquierda y la derecha espacial y la creación de reflejo.</span><span class="sxs-lookup"><span data-stu-id="d1afe-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="d1afe-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="d1afe-105">CLSID</span></span>

<span data-ttu-id="d1afe-106">CLSID \_ VideoProcessorMFT</span><span class="sxs-lookup"><span data-stu-id="d1afe-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="d1afe-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d1afe-107">Interfaces</span></span>

-   [<span data-ttu-id="d1afe-108">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="d1afe-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="d1afe-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="d1afe-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="d1afe-110">**IMFVideoProcessorControl**</span><span class="sxs-lookup"><span data-stu-id="d1afe-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="d1afe-111">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="d1afe-111">Input Formats</span></span>

-   <span data-ttu-id="d1afe-112">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="d1afe-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="d1afe-113">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="d1afe-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="d1afe-114">**MFVideoFormat \_ i420**</span><span class="sxs-lookup"><span data-stu-id="d1afe-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="d1afe-115">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="d1afe-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="d1afe-116">**MFVideoFormat \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="d1afe-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="d1afe-117">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="d1afe-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="d1afe-118">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="d1afe-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="d1afe-119">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="d1afe-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="d1afe-120">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="d1afe-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="d1afe-121">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="d1afe-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="d1afe-122">**MFVideoFormat \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="d1afe-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="d1afe-123">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="d1afe-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="d1afe-124">**MFVideoFormat \_ V410**</span><span class="sxs-lookup"><span data-stu-id="d1afe-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="d1afe-125">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="d1afe-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="d1afe-126">**MFVideoFormat \_ Y41P**</span><span class="sxs-lookup"><span data-stu-id="d1afe-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="d1afe-127">**MFVideoFormat \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="d1afe-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="d1afe-128">**MFVideoFormat \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="d1afe-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="d1afe-129">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="d1afe-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="d1afe-130">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="d1afe-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="d1afe-131">**MFVideoFormat \_ YVYU**</span><span class="sxs-lookup"><span data-stu-id="d1afe-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="d1afe-132">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="d1afe-132">Output Formats</span></span>

-   <span data-ttu-id="d1afe-133">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="d1afe-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="d1afe-134">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="d1afe-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="d1afe-135">**MFVideoFormat \_ i420**</span><span class="sxs-lookup"><span data-stu-id="d1afe-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="d1afe-136">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="d1afe-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="d1afe-137">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="d1afe-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="d1afe-138">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="d1afe-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="d1afe-139">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="d1afe-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="d1afe-140">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="d1afe-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="d1afe-141">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="d1afe-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="d1afe-142">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="d1afe-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="d1afe-143">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="d1afe-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="d1afe-144">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="d1afe-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="d1afe-145">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="d1afe-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="d1afe-146">No se admiten todas las combinaciones de formatos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="d1afe-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="d1afe-147">Para probar si se admite una conversión, establezca el tipo de entrada y, a continuación, llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="d1afe-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="d1afe-148">Para obtener más información sobre estos formatos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d1afe-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1afe-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1afe-149">Remarks</span></span>

<span data-ttu-id="d1afe-150">Se puede crear una instancia del procesador de vídeo de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="d1afe-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="d1afe-151">Llamando a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="d1afe-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="d1afe-152">El procesador de vídeo se registra en la categoría **MFT \_ categoría de \_ \_ procesador de vídeo** .</span><span class="sxs-lookup"><span data-stu-id="d1afe-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="d1afe-153">Llamando a la función de COM **CoCreateInstance** pasándole el CLSID CLSID **\_ VideoProcessorMFT**.</span><span class="sxs-lookup"><span data-stu-id="d1afe-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="d1afe-154">Los comentarios siguientes se refieren al trabajo con rectángulos de origen y rectángulos de destino en la **MFT del procesador de vídeo**.</span><span class="sxs-lookup"><span data-stu-id="d1afe-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="d1afe-155">Los rectángulos de origen y de destino se establecen con [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) y [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) y algunas veces con [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span><span class="sxs-lookup"><span data-stu-id="d1afe-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="d1afe-156">El rectángulo de origen se debe alinear y redondear para que coincida con los requisitos del formato de color del fotograma que se encuentra en el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d1afe-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="d1afe-157">Esto es importante porque los formatos como 420 y 422 tienen requisitos sobre las dimensiones y los desplazamientos que se pueden crear y a los que se puede tener acceso.</span><span class="sxs-lookup"><span data-stu-id="d1afe-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="d1afe-158">Por ejemplo, un rectángulo de origen de {1, 0, 319, 240} (izquierda, superior, derecha, inferior) se redondeará a {2, 0, 320, 240} cuando el formato de entrada sea 420.</span><span class="sxs-lookup"><span data-stu-id="d1afe-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="d1afe-159">Tanto el rectángulo de origen como el de destino siempre se fijarán para caber dentro de sus marcos respectivos, el rectángulo de origen y el rectángulo de destino hasta el marco de destino.</span><span class="sxs-lookup"><span data-stu-id="d1afe-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="d1afe-160">Esto significa que los valores negativos no son significativos; siempre se fijarán en 0.</span><span class="sxs-lookup"><span data-stu-id="d1afe-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="d1afe-161">El rectángulo de origen se encuentra en el sistema de coordenadas del marco de destino, menos cualquier rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="d1afe-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="d1afe-162">Esto significa que las transformaciones como la rotación se "deshacen" en el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="d1afe-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="d1afe-163">Por lo tanto, no es necesario saber si el vídeo se ha girado o si se ha desempaquetado 3D.</span><span class="sxs-lookup"><span data-stu-id="d1afe-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="d1afe-164">Por ejemplo, puede dibujar un rectángulo en la parte superior de la etiqueta de vídeo, tomar las coordenadas relativas (con respecto a la etiqueta de vídeo), normalizarlas (intervalo de 0 a 1) y pasarlas como rectángulo de origen y deben funcionar según lo previsto, incluso si el vídeo se está girando.</span><span class="sxs-lookup"><span data-stu-id="d1afe-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="d1afe-165">El procesador de vídeo admite el procesamiento de vídeo acelerado mediante GPU con Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d1afe-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="d1afe-166">Para obtener más información, consulte [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="d1afe-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="d1afe-167">Vídeo de Stereoscopic</span><span class="sxs-lookup"><span data-stu-id="d1afe-167">Stereoscopic Video</span></span>

<span data-ttu-id="d1afe-168">El procesador de vídeo admite la operación ver desempaquetado en fotogramas de vídeo 3D:</span><span class="sxs-lookup"><span data-stu-id="d1afe-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="d1afe-169">Si el marco de entrada contiene dos vistas empaquetadas en el mismo fotograma, el procesador de vídeo puede dividir las vistas en búferes independientes, o bien extraer la vista base y descartar la segunda vista.</span><span class="sxs-lookup"><span data-stu-id="d1afe-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="d1afe-170">Para habilitar ver desempaquetado, establezca el atributo [MF \_ enable \_ 3DVIDEO \_ Output](mf-enable-3dvideo-output.md) en **MF3DVideoOutputType \_ Stereo** o **MF3DVideoOutputType \_ BaseView**.</span><span class="sxs-lookup"><span data-stu-id="d1afe-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1afe-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1afe-171">Requirements</span></span>



| <span data-ttu-id="d1afe-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1afe-172">Requirement</span></span> | <span data-ttu-id="d1afe-173">Value</span><span class="sxs-lookup"><span data-stu-id="d1afe-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1afe-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1afe-174">Header</span></span><br/> | <dl> <span data-ttu-id="d1afe-175"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1afe-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1afe-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1afe-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1afe-177">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="d1afe-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




