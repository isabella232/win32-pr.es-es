---
title: Configuración de secuencias de vídeo
description: Configuración de secuencias de vídeo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flujos, configurar secuencias de vídeo
- códecs, configurar secuencias de vídeo
- secuencias de vídeo, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695533"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="35435-106">Configuración de secuencias de vídeo</span><span class="sxs-lookup"><span data-stu-id="35435-106">Configuring Video Streams</span></span>

<span data-ttu-id="35435-107">Las secuencias de vídeo son más flexibles en su configuración que las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="35435-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="35435-108">Esto se debe a que las propiedades de los fotogramas que componen el vídeo pueden variar considerablemente de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="35435-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="35435-109">Al recuperar el formato de códec para el códec que está utilizando, debe establecer los siguientes valores para los objetos de configuración de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="35435-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="35435-110">Value</span><span class="sxs-lookup"><span data-stu-id="35435-110">Value</span></span>                                 | <span data-ttu-id="35435-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="35435-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35435-112">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="35435-112">Bit rate</span></span>                              | <span data-ttu-id="35435-113">Llame a [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) para establecer en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="35435-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="35435-114">El códec de vídeo intentará comprimir el medio para cumplir sus especificaciones.</span><span class="sxs-lookup"><span data-stu-id="35435-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="35435-115">Si los valores son demasiado bajos, el vídeo comprimido resultante será muy degradado.</span><span class="sxs-lookup"><span data-stu-id="35435-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="35435-116">Ventana de búfer</span><span class="sxs-lookup"><span data-stu-id="35435-116">Buffer window</span></span>                         | <span data-ttu-id="35435-117">Llame a [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) para establecer en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="35435-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="35435-118">El códec de vídeo intentará comprimir el medio para cumplir sus especificaciones.</span><span class="sxs-lookup"><span data-stu-id="35435-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="35435-119">Si los valores son demasiado bajos, el vídeo comprimido resultante será muy degradado.</span><span class="sxs-lookup"><span data-stu-id="35435-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="35435-120">**WMVIDEOINFOHEADER.rcSource**</span><span class="sxs-lookup"><span data-stu-id="35435-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="35435-121">La esquina superior izquierda debe establecerse en 0, 0.</span><span class="sxs-lookup"><span data-stu-id="35435-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="35435-122">La esquina inferior derecha debe establecerse en las dimensiones del marco.</span><span class="sxs-lookup"><span data-stu-id="35435-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="35435-123">Por ejemplo, en una secuencia de 640 x 480, esta configuración sería 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="35435-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="35435-124">**WMVIDEOINFOHEADER.rcTarget**</span><span class="sxs-lookup"><span data-stu-id="35435-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="35435-125">Debe coincidir con **rcSource**.</span><span class="sxs-lookup"><span data-stu-id="35435-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="35435-126">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="35435-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="35435-127">Debe coincidir con el conjunto de velocidad de bits para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="35435-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="35435-128">**WMVIDEOINFOHEADER. AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="35435-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="35435-129">Se establece en el tiempo aproximado por fotograma.</span><span class="sxs-lookup"><span data-stu-id="35435-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="35435-130">**BITMAPINFOHEADER. biwidth**</span><span class="sxs-lookup"><span data-stu-id="35435-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="35435-131">Se establece en el ancho, en píxeles, del tamaño del fotograma deseado.</span><span class="sxs-lookup"><span data-stu-id="35435-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="35435-132">**BITMAPINFOHEADER. biheight**</span><span class="sxs-lookup"><span data-stu-id="35435-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="35435-133">Se establece en el alto, en píxeles, del tamaño del fotograma deseado.</span><span class="sxs-lookup"><span data-stu-id="35435-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="35435-134">El contenido de vídeo no se reproduce correctamente a menos que esté codificado en un tamaño que sea un múltiplo de cuatro para ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="35435-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="35435-135">La excepción es un vídeo [*RGB*](wmformat-glossary.md) sin comprimir, que puede tener cualquier tamaño.</span><span class="sxs-lookup"><span data-stu-id="35435-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="35435-136">Si intenta establecer un tamaño que no sea múltiplo de cuatro, el escritor devolverá uno de los siguientes errores:</span><span class="sxs-lookup"><span data-stu-id="35435-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="35435-137">\_formato de \_ entrada no válido de NS E \_ \_</span><span class="sxs-lookup"><span data-stu-id="35435-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="35435-138">\_formato de salida NS E \_ no válido \_ \_</span><span class="sxs-lookup"><span data-stu-id="35435-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="35435-139">NS \_ E \_ INVALIDPROFILE</span><span class="sxs-lookup"><span data-stu-id="35435-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="35435-140">Si utiliza codificación de velocidad de bits variable, puede que necesite realizar otros ajustes.</span><span class="sxs-lookup"><span data-stu-id="35435-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="35435-141">Para obtener más información, consulte [configuración de secuencias VBR](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="35435-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="35435-142">Algunos códecs de Windows Media Video admiten varios niveles de complejidad.</span><span class="sxs-lookup"><span data-stu-id="35435-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="35435-143">Los niveles de complejidad determinan los algoritmos que usará el códec al codificar una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="35435-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="35435-144">El uso de un nivel de complejidad alto requiere más capacidad de procesamiento para la codificación y la descodificación.</span><span class="sxs-lookup"><span data-stu-id="35435-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="35435-145">Cada códec que admite la configuración de complejidad expone la configuración siguiente que puede recuperar con el método [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="35435-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="35435-146">Configuración</span><span class="sxs-lookup"><span data-stu-id="35435-146">Setting</span></span>                 | <span data-ttu-id="35435-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="35435-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="35435-148">g \_ wszComplexityMax</span><span class="sxs-lookup"><span data-stu-id="35435-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="35435-149">El nivel de calidad máximo admitido por el códec.</span><span class="sxs-lookup"><span data-stu-id="35435-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="35435-150">g \_ wszComplexityOffline</span><span class="sxs-lookup"><span data-stu-id="35435-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="35435-151">El nivel de calidad sugerido para la reproducción sin conexión.</span><span class="sxs-lookup"><span data-stu-id="35435-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="35435-152">g \_ wszComplexityLive</span><span class="sxs-lookup"><span data-stu-id="35435-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="35435-153">El nivel de calidad sugerido para la reproducción en streaming.</span><span class="sxs-lookup"><span data-stu-id="35435-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="35435-154">Para establecer la complejidad de una secuencia de vídeo en un perfil, use el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) con la propiedad g \_ wszComplexity.</span><span class="sxs-lookup"><span data-stu-id="35435-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="35435-155">El valor que establezca debe ser menor o igual que la complejidad máxima admitida para el códec.</span><span class="sxs-lookup"><span data-stu-id="35435-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35435-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35435-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35435-157">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="35435-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="35435-158">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="35435-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="35435-159">**Configuración de complejidad de vídeo**</span><span class="sxs-lookup"><span data-stu-id="35435-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




