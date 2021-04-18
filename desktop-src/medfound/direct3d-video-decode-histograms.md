---
description: Este artículo contiene instrucciones para generar histogramas al descodificar vídeo con las API de vídeo Direct3D 11 o 12.
ms.assetid: ''
title: Histogramas de descodificación de vídeo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720288"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="3630b-103">Histogramas de descodificación de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="3630b-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="3630b-104">Este artículo contiene instrucciones para generar histogramas al descodificar vídeo con las API de vídeo Direct3D 11 o 12.</span><span class="sxs-lookup"><span data-stu-id="3630b-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="3630b-105">Comprobar el dispositivo de vídeo para las funcionalidades de histograma</span><span class="sxs-lookup"><span data-stu-id="3630b-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="3630b-106">Antes de intentar generar histogramas, debe comprobar si el dispositivo de vídeo actual es compatible con la característica de histograma de descodificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3630b-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="3630b-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3630b-107">Direct3D 12</span></span>

<span data-ttu-id="3630b-108">Llame a [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para comprobar los detalles de compatibilidad de las operaciones de descodificación de vídeo de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3630b-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="3630b-109">Pase el valor **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** de la enumeración [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar que está solicitando compatibilidad con histogramas de descodificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3630b-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="3630b-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3630b-110">Direct3D 11</span></span>

<span data-ttu-id="3630b-111">Llame a [ID3D11VideoDevice2:: CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) y pase el valor **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** del [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) para determinar si se admiten histogramas para el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="3630b-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="3630b-112">Habilitar histograma durante la descodificación</span><span class="sxs-lookup"><span data-stu-id="3630b-112">Enabling histogram during decode</span></span>

<span data-ttu-id="3630b-113">La colección de datos de histograma está habilitada por el llamador que proporciona los búferes en los que se almacenan los datos del histograma.</span><span class="sxs-lookup"><span data-stu-id="3630b-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="3630b-114">Un búfer de salida de histograma nulo para un componente determinado indica que la colección de histograma está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="3630b-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="3630b-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3630b-115">Direct3D 12</span></span>

<span data-ttu-id="3630b-116">Con el fin de proporcionar búferes de salida para recibir datos de histogramas mediante Direct3D 12, debe crear la lista de comandos de descodificación con el método [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) .</span><span class="sxs-lookup"><span data-stu-id="3630b-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="3630b-117">Este método toma una estructura de [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) como argumento.</span><span class="sxs-lookup"><span data-stu-id="3630b-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="3630b-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** tiene un campo de tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), que permite especificar un [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) en el que se generan los datos de histograma.</span><span class="sxs-lookup"><span data-stu-id="3630b-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="3630b-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3630b-119">Direct3D 11</span></span>

<span data-ttu-id="3630b-120">La interfaz [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) proporciona el método [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , que permite proporcionar una o más interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) en las que se generarán los datos del histograma.</span><span class="sxs-lookup"><span data-stu-id="3630b-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="3630b-121">El [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) para especificar los componentes para los que desea que se generen los datos del histograma.</span><span class="sxs-lookup"><span data-stu-id="3630b-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="3630b-122">Formato de búfer</span><span class="sxs-lookup"><span data-stu-id="3630b-122">Buffer format</span></span>

<span data-ttu-id="3630b-123">La salida del histograma de descodificación se escribe en un búfer como un contador entero por componente.</span><span class="sxs-lookup"><span data-stu-id="3630b-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="3630b-124">El formato de búfer es un valor de 32 bits por ubicación.</span><span class="sxs-lookup"><span data-stu-id="3630b-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="3630b-125">Un dispositivo puede usar una profundidad de bits de contador de entero menor que 32 bits, pero debe ser de 16, 24 o 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3630b-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="3630b-126">Si es así, el valor del contador se almacena en los bits inferiores y los bits no usados superiores son cero.</span><span class="sxs-lookup"><span data-stu-id="3630b-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="3630b-127">Cuando el recuento de un bin supera el valor máximo, el dispositivo establece el valor máximo en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3630b-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="3630b-128">Los dispositivos informan del número de ubicaciones admitidas, que debe ser un valor que sea una potencia de 2.</span><span class="sxs-lookup"><span data-stu-id="3630b-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="3630b-129">El número mínimo de ubicaciones necesarias para los dispositivos que admiten esta característica es 64.</span><span class="sxs-lookup"><span data-stu-id="3630b-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="3630b-130">Debe proporcionar un búfer con un desplazamiento alineado de 256 bytes y un tamaño que sea el número admitido de depósitos multiplicado por el tamaño de la ubicación (4 bytes) para cada componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="3630b-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="3630b-131">La ubicación de la ubicación viene determinada por:</span><span class="sxs-lookup"><span data-stu-id="3630b-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="3630b-132">Cuando un formato define los bits útiles de un componente como menor que el número de bits de almacenamiento (por ejemplo, P010 usa los 10 bits superiores de 16 bits de almacenamiento de componentes), solo se tienen en cuenta los bits útiles (P010 se trata como un valor de 10 bits).</span><span class="sxs-lookup"><span data-stu-id="3630b-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="3630b-133">El dispositivo de vídeo informa de los componentes que se admiten.</span><span class="sxs-lookup"><span data-stu-id="3630b-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="3630b-134">Si el autor de la llamada no desea un histograma para un componente determinado, especifica nullptr.</span><span class="sxs-lookup"><span data-stu-id="3630b-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="3630b-135">Si el controlador no admite un histograma para un componente determinado, el búfer del histograma del componente debe ser nullptr.</span><span class="sxs-lookup"><span data-stu-id="3630b-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="3630b-136">Cuando se admiten varios componentes, la aplicación puede solicitar cualquier combinación de componentes por descodificación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="3630b-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="3630b-137">Por ejemplo, si el hardware informa de la compatibilidad con los componentes Y, U y V, la aplicación puede solicitar el histograma Y solo para el fotograma uno, el histograma U solo para el fotograma dos y el histograma V solo para el fotograma 3.</span><span class="sxs-lookup"><span data-stu-id="3630b-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="3630b-138">También pueden solicitar cualquier combinación de dos componentes o de los tres componentes.</span><span class="sxs-lookup"><span data-stu-id="3630b-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="3630b-139">Las aplicaciones proporcionan un desplazamiento independiente y un puntero/identificador de búfer para cada componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="3630b-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="3630b-140">Este puntero puede apuntar al mismo recurso que otro componente o a un recurso independiente.</span><span class="sxs-lookup"><span data-stu-id="3630b-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="3630b-141">El desplazamiento permite colocar varios componentes en el mismo búfer, pero la región de salida especificada por el desplazamiento y el tamaño del histograma no deben superponerse a otra salida de componente de histograma.</span><span class="sxs-lookup"><span data-stu-id="3630b-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="3630b-142">El histograma también se puede escribir en el mismo búfer que otro contenido no relacionado, como cuando se usa en una estrategia de subasignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="3630b-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="3630b-143">El tiempo de ejecución de D3D valida que los llamadores solo habilitan el histograma para los componentes compatibles, que el desplazamiento del búfer está alineado y que el tamaño del búfer es suficiente para el número de ubicaciones proporcionado.</span><span class="sxs-lookup"><span data-stu-id="3630b-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="3630b-144">Contenido protegido</span><span class="sxs-lookup"><span data-stu-id="3630b-144">Protected content</span></span>

<span data-ttu-id="3630b-145">Los búferes del histograma deben tener la misma protección de superficie que la superficie de salida de descodificación.</span><span class="sxs-lookup"><span data-stu-id="3630b-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="3630b-146">Si la superficie de salida de descodificación no es un recurso protegido, el búfer de histograma no debe ser un recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="3630b-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="3630b-147">Si la superficie de salida descodificada es recurso protegido, el histograma debe ser un recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="3630b-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="3630b-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3630b-148">Related topics</span></span>

<dl> <span data-ttu-id="3630b-149"><dt>API de vídeo de 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="3630b-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 




