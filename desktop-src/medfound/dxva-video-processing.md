---
description: El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Procesamiento de vídeo de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539561"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="efde3-104">Procesamiento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="efde3-104">DXVA Video Processing</span></span>

<span data-ttu-id="efde3-105">El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="efde3-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="efde3-106">Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="efde3-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="efde3-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="efde3-108">Información general</span><span class="sxs-lookup"><span data-stu-id="efde3-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="efde3-109">Creación de un dispositivo de procesamiento de vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="efde3-110">Obtener el puntero IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="efde3-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="efde3-111">Enumerar los dispositivos de procesamiento de vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="efde3-112">Enumerar formatos de Render-Target</span><span class="sxs-lookup"><span data-stu-id="efde3-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="efde3-113">Consultar las capacidades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="efde3-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="efde3-114">Crear el dispositivo</span><span class="sxs-lookup"><span data-stu-id="efde3-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="efde3-115">Proceso de vídeo blit</span><span class="sxs-lookup"><span data-stu-id="efde3-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="efde3-116">Parámetros de blit</span><span class="sxs-lookup"><span data-stu-id="efde3-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="efde3-117">Ejemplos de entrada</span><span class="sxs-lookup"><span data-stu-id="efde3-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="efde3-118">Composición de imagen</span><span class="sxs-lookup"><span data-stu-id="efde3-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="efde3-119">Ejemplo 1: panorámica</span><span class="sxs-lookup"><span data-stu-id="efde3-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="efde3-120">Ejemplo 2: expandir imágenes de subflujo</span><span class="sxs-lookup"><span data-stu-id="efde3-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="efde3-121">Ejemplo 3: alto de flujo no coincidente</span><span class="sxs-lookup"><span data-stu-id="efde3-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="efde3-122">Ejemplo 4: rectángulo de destino menor que la superficie de destino</span><span class="sxs-lookup"><span data-stu-id="efde3-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="efde3-123">Ejemplo 5: rectángulos de origen</span><span class="sxs-lookup"><span data-stu-id="efde3-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="efde3-124">Ejemplo 6: intersección de rectángulos de destino</span><span class="sxs-lookup"><span data-stu-id="efde3-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="efde3-125">Ejemplo 7: expandir y recortar vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="efde3-126">Orden de ejemplo de entrada</span><span class="sxs-lookup"><span data-stu-id="efde3-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="efde3-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="efde3-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="efde3-128">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="efde3-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="efde3-129">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="efde3-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="efde3-130">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="efde3-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="efde3-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efde3-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="efde3-132">Información general</span><span class="sxs-lookup"><span data-stu-id="efde3-132">Overview</span></span>

<span data-ttu-id="efde3-133">El hardware gráfico puede usar la unidad de procesamiento de gráficos (GPU) para procesar imágenes de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="efde3-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="efde3-134">Un dispositivo de *procesamiento de vídeo* es un componente de software que encapsula estas funciones.</span><span class="sxs-lookup"><span data-stu-id="efde3-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="efde3-135">Las aplicaciones pueden usar un dispositivo de procesamiento de vídeo para realizar funciones como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="efde3-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="efde3-136">Desentrelazado y Telecine inverso</span><span class="sxs-lookup"><span data-stu-id="efde3-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="efde3-137">Combinación de subsecuencias de vídeo en la imagen de vídeo principal</span><span class="sxs-lookup"><span data-stu-id="efde3-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="efde3-138">Ajuste de color (ProcAmp) y filtrado de imágenes</span><span class="sxs-lookup"><span data-stu-id="efde3-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="efde3-139">Escalado de imágenes</span><span class="sxs-lookup"><span data-stu-id="efde3-139">Image scaling</span></span>
-   <span data-ttu-id="efde3-140">Conversión de espacio de colores</span><span class="sxs-lookup"><span data-stu-id="efde3-140">Color-space conversion</span></span>
-   <span data-ttu-id="efde3-141">Combinación alfa</span><span class="sxs-lookup"><span data-stu-id="efde3-141">Alpha blending</span></span>

<span data-ttu-id="efde3-142">En el diagrama siguiente se muestran las fases de la canalización de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="efde3-143">El diagrama no está diseñado para mostrar una implementación real.</span><span class="sxs-lookup"><span data-stu-id="efde3-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="efde3-144">Por ejemplo, el controlador de gráficos puede combinar varias fases en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="efde3-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="efde3-145">Todas estas operaciones se pueden realizar en una única llamada al dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="efde3-146">Algunas de las fases que se muestran aquí, como el filtrado de ruido y detalles, pueden no ser compatibles con el controlador.</span><span class="sxs-lookup"><span data-stu-id="efde3-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![diagrama que muestra las fases del procesamiento de vídeo de DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="efde3-148">La entrada de la canalización de procesamiento de vídeo siempre incluye una secuencia de vídeo *principal* , que contiene los datos de imagen principales.</span><span class="sxs-lookup"><span data-stu-id="efde3-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="efde3-149">La secuencia de vídeo principal determina la velocidad de fotogramas del vídeo de salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="efde3-150">Cada fotograma del vídeo de salida se calcula en relación con los datos de entrada de la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="efde3-151">Los píxeles del flujo principal siempre son opacos, sin datos alfa por píxel.</span><span class="sxs-lookup"><span data-stu-id="efde3-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="efde3-152">La secuencia de vídeo principal puede ser progresiva o entrelazada.</span><span class="sxs-lookup"><span data-stu-id="efde3-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="efde3-153">Opcionalmente, la canalización de procesamiento de vídeo puede recibir hasta 15 subsecuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="efde3-154">Un subflujo contiene datos de imagen auxiliares, como subtítulos (CC) o subimágenes de DVD.</span><span class="sxs-lookup"><span data-stu-id="efde3-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="efde3-155">Estas imágenes se muestran en el flujo de vídeo principal y, por lo general, no están pensadas para que se muestren por sí mismas.</span><span class="sxs-lookup"><span data-stu-id="efde3-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="efde3-156">Las imágenes de subflujo pueden contener datos alfa por píxel y siempre son fotogramas progresivos.</span><span class="sxs-lookup"><span data-stu-id="efde3-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="efde3-157">El dispositivo de procesamiento de vídeo alfa combina las imágenes de subflujo con el fotograma desentrelazado actual de la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="efde3-158">En el resto de este tema, el término *imagen* se usa para los datos de entrada en un dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="efde3-159">Una imagen puede constar de un fotograma progresivo, un solo campo o dos campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="efde3-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="efde3-160">La salida siempre es un marco desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="efde3-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="efde3-161">Un controlador de vídeo puede implementar más de un dispositivo de procesamiento de vídeo para proporcionar diferentes conjuntos de capacidades de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="efde3-162">Los dispositivos se identifican mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="efde3-162">Devices are identified by GUID.</span></span> <span data-ttu-id="efde3-163">Los siguientes GUID están predefinidos:</span><span class="sxs-lookup"><span data-stu-id="efde3-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="efde3-164">**DXVA2 \_ VideoProcBobDevice**.</span><span class="sxs-lookup"><span data-stu-id="efde3-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="efde3-165">Este dispositivo realiza el desentrelazado de Bob.</span><span class="sxs-lookup"><span data-stu-id="efde3-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="efde3-166">**DXVA2 \_ VideoProcProgressiveDevice**.</span><span class="sxs-lookup"><span data-stu-id="efde3-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="efde3-167">Este dispositivo se usa si el vídeo solo contiene fotogramas progresivos, sin fotogramas entrelazados.</span><span class="sxs-lookup"><span data-stu-id="efde3-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="efde3-168">(Algunos contenidos de vídeo contienen una mezcla de fotogramas progresivos y entrelazados.</span><span class="sxs-lookup"><span data-stu-id="efde3-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="efde3-169">No se puede usar el dispositivo progresivo para este tipo de contenido de vídeo "mixto", ya que se requiere un paso de desentrelazado para los fotogramas entrelazados).</span><span class="sxs-lookup"><span data-stu-id="efde3-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="efde3-170">Cada controlador de gráficos que admite el procesamiento de vídeo de DXVA debe implementar al menos estos dos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="efde3-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="efde3-171">El controlador de gráficos también puede proporcionar otros dispositivos, que se identifican mediante GUID específicos del controlador.</span><span class="sxs-lookup"><span data-stu-id="efde3-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="efde3-172">Por ejemplo, un controlador podría implementar un algoritmo de desentrelazado de propiedad que genera una salida de mejor calidad que el desentrelazado de Bob.</span><span class="sxs-lookup"><span data-stu-id="efde3-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="efde3-173">Algunos algoritmos de desentrelazado pueden requerir imágenes de referencia hacia delante o hacia atrás desde el flujo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="efde3-174">Si es así, el autor de la llamada debe proporcionar estas imágenes al controlador en la secuencia correcta, tal y como se describe más adelante en esta sección.</span><span class="sxs-lookup"><span data-stu-id="efde3-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="efde3-175">También se proporciona un dispositivo de software de referencia.</span><span class="sxs-lookup"><span data-stu-id="efde3-175">A reference software device is also provided.</span></span> <span data-ttu-id="efde3-176">El dispositivo de software está optimizado para la calidad en lugar de la velocidad y puede no ser adecuado para el procesamiento de vídeo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="efde3-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="efde3-177">El dispositivo de software de referencia usa el valor de GUID DXVA2 \_ VideoProcSoftwareDevice.</span><span class="sxs-lookup"><span data-stu-id="efde3-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="efde3-178">Creación de un dispositivo de procesamiento de vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="efde3-179">Antes de usar el procesamiento de vídeo de DXVA, la aplicación debe crear un dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="efde3-180">Esta es una breve descripción de los pasos, que se explican con mayor detalle en el resto de esta sección:</span><span class="sxs-lookup"><span data-stu-id="efde3-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="efde3-181">Obtiene un puntero a la interfaz [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .</span><span class="sxs-lookup"><span data-stu-id="efde3-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="efde3-182">Cree una descripción del formato de vídeo para la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="efde3-183">Use esta descripción para obtener una lista de los dispositivos de procesamiento de vídeo que admiten el formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="efde3-184">Los dispositivos se identifican mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="efde3-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="efde3-185">Para un dispositivo determinado, obtenga una lista de formatos de destino de representación admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efde3-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="efde3-186">Los formatos se devuelven como una lista de valores de **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="efde3-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="efde3-187">Si tiene previsto mezclar subsecuencias, obtenga también una lista de los formatos de subflujo admitidos.</span><span class="sxs-lookup"><span data-stu-id="efde3-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="efde3-188">Consultar las capacidades de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efde3-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="efde3-189">Cree el dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-189">Create the video processing device.</span></span>

<span data-ttu-id="efde3-190">En ocasiones, puede omitir algunos de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="efde3-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="efde3-191">Por ejemplo, en lugar de obtener la lista de formatos de destino de representación, puede intentar simplemente crear el dispositivo de procesamiento de vídeo con el formato que prefiera y ver si se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="efde3-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="efde3-192">Un formato común, como D3DFMT \_ X8R8G8B8, es probable que se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="efde3-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="efde3-193">En el resto de esta sección se describen estos pasos con detalle.</span><span class="sxs-lookup"><span data-stu-id="efde3-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="efde3-194">Obtener el puntero IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="efde3-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="efde3-195">La interfaz [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) se obtiene del dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="efde3-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="efde3-196">Hay dos maneras de obtener un puntero a esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="efde3-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="efde3-197">Desde un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="efde3-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="efde3-198">Desde la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="efde3-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="efde3-199">Si tiene un puntero a un dispositivo Direct3D, puede obtener un puntero [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) llamando a la función [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) .</span><span class="sxs-lookup"><span data-stu-id="efde3-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="efde3-200">Pase un puntero a la interfaz **IDirect3DDevice9** del dispositivo y especifique **IID \_ IDirectXVideoProcessorService** para el parámetro *riid* , tal y como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="efde3-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="efde3-201">en algunos casos, un objeto crea el dispositivo Direct3D y, a continuación, lo comparte con otros objetos a través del [Administrador de dispositivos de Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="efde3-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="efde3-202">En esta situación, puede llamar a [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) en el administrador de dispositivos para obtener el puntero [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="efde3-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="efde3-203">Enumerar los dispositivos de procesamiento de vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="efde3-204">Para obtener una lista de dispositivos de procesamiento de vídeo, rellene una estructura [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) con el formato de la secuencia de vídeo principal y pase esta estructura al método [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) .</span><span class="sxs-lookup"><span data-stu-id="efde3-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="efde3-205">El método devuelve una matriz de GUID, uno para cada dispositivo de procesamiento de vídeo que se puede usar con este formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="efde3-206">Considere una aplicación que representa una secuencia de vídeo en formato YUY2, con la definición BT. 709 del color YUV, con una velocidad de fotogramas de 29,97 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="efde3-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="efde3-207">Supongamos que el contenido de vídeo se compone exclusivamente de tramas progresivas.</span><span class="sxs-lookup"><span data-stu-id="efde3-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="efde3-208">En el fragmento de código siguiente se muestra cómo rellenar la descripción del formato y obtener los GUID del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="efde3-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="efde3-209">El código de este ejemplo se toma del ejemplo de SDK de [ \_ videoproc DXVA2](dxva2-videoproc-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="efde3-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="efde3-210">La matriz *pGuids* de este ejemplo se asigna mediante el método [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , por lo que la aplicación debe liberar la matriz llamando a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="efde3-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="efde3-211">El resto de los pasos se pueden realizar con cualquiera de los GUID de dispositivo devueltos por este método.</span><span class="sxs-lookup"><span data-stu-id="efde3-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="efde3-212">Enumerar formatos de Render-Target</span><span class="sxs-lookup"><span data-stu-id="efde3-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="efde3-213">Para obtener la lista de formatos de destino de representación admitidos por el dispositivo, pase el GUID del dispositivo y la estructura [**DXVA2 de \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) al método [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , tal y como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="efde3-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="efde3-214">El método devuelve una matriz de valores **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="efde3-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="efde3-215">En este ejemplo, donde el tipo de entrada es YUY2, una lista típica de formatos podría ser D3DFMT \_ X8R8G8B8 (RGB de 32 bits) y D3DMFT \_ YUY2 (el formato de entrada).</span><span class="sxs-lookup"><span data-stu-id="efde3-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="efde3-216">Sin embargo, la lista exacta dependerá del controlador.</span><span class="sxs-lookup"><span data-stu-id="efde3-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="efde3-217">La lista de formatos disponibles para las subsecuencias puede variar en función del formato de destino de representación y el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="efde3-218">Para obtener la lista de formatos de subsecuencia, pase el GUID del dispositivo, la estructura de formato y el formato de representación-destino al método [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , tal y como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="efde3-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="efde3-219">Este método devuelve otra matriz de valores **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="efde3-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="efde3-220">Los formatos de subflujo típicos son AYUV y AI44.</span><span class="sxs-lookup"><span data-stu-id="efde3-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="efde3-221">Consultar las capacidades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="efde3-221">Query the Device Capabilities</span></span>

<span data-ttu-id="efde3-222">Para obtener las capacidades de un dispositivo determinado, pase el GUID del dispositivo, la estructura de formato y un formato de destino de representación al método [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) .</span><span class="sxs-lookup"><span data-stu-id="efde3-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="efde3-223">El método rellena una estructura de estructura de [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efde3-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="efde3-224">Crear el dispositivo</span><span class="sxs-lookup"><span data-stu-id="efde3-224">Create the Device</span></span>

<span data-ttu-id="efde3-225">Para crear el dispositivo de procesamiento de vídeo, llame a [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span><span class="sxs-lookup"><span data-stu-id="efde3-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="efde3-226">La entrada a este método es el GUID del dispositivo, la descripción del formato, el formato del destino de representación y el número máximo de subflujos que se van a mezclar.</span><span class="sxs-lookup"><span data-stu-id="efde3-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="efde3-227">El método devuelve un puntero a la interfaz [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , que representa el dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="efde3-228">Proceso de vídeo blit</span><span class="sxs-lookup"><span data-stu-id="efde3-228">Video Process Blit</span></span>

<span data-ttu-id="efde3-229">La operación principal de procesamiento de vídeo es el *procesamiento de vídeo*.</span><span class="sxs-lookup"><span data-stu-id="efde3-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="efde3-230">(Un *blit* es cualquier operación que combina dos o más mapas de bits en un único mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="efde3-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="efde3-231">Un blit de procesamiento de vídeo combina imágenes de entrada para crear un fotograma de salida.) Para realizar una blit de procesamiento de vídeo, llame a [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="efde3-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="efde3-232">Este método pasa un conjunto de muestras de vídeo al dispositivo de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="efde3-233">En respuesta, el dispositivo de procesamiento de vídeo procesa las imágenes de entrada y genera un fotograma de salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="efde3-234">El procesamiento puede incluir desentrelazado, conversión de espacio de color y combinación de subflujo.</span><span class="sxs-lookup"><span data-stu-id="efde3-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="efde3-235">La salida se escribe en una superficie de destino proporcionada por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="efde3-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="efde3-236">El método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="efde3-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="efde3-237">*pRT* apunta a una superficie de destino de representación de **IDirect3DSurface9** que recibirá el fotograma de vídeo procesado.</span><span class="sxs-lookup"><span data-stu-id="efde3-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="efde3-238">*pBltParams* apunta a una [**estructura \_ VideoProcessBltParams de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) que especifica los parámetros para el blit.</span><span class="sxs-lookup"><span data-stu-id="efde3-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="efde3-239">*pSamples* es la dirección de una matriz de estructuras de [**\_ videoejemplo de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="efde3-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="efde3-240">Estas estructuras contienen los ejemplos de entrada para el blit.</span><span class="sxs-lookup"><span data-stu-id="efde3-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="efde3-241">*NumSamples* proporciona el tamaño de la matriz de *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="efde3-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="efde3-242">El parámetro *Reserved* está reservado y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="efde3-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="efde3-243">En la matriz *pSamples* , el llamador debe proporcionar los siguientes ejemplos de entrada:</span><span class="sxs-lookup"><span data-stu-id="efde3-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="efde3-244">La imagen actual de la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="efde3-245">Imágenes de referencia hacia delante y hacia atrás, si es necesario para el algoritmo de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="efde3-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="efde3-246">Cero o más imágenes de subsecuencia, hasta un máximo de 15 subsecuencias.</span><span class="sxs-lookup"><span data-stu-id="efde3-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="efde3-247">El controlador espera que esta matriz esté en un orden determinado, tal como se describe en [orden de ejemplo de entrada](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="efde3-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="efde3-248">Parámetros de blit</span><span class="sxs-lookup"><span data-stu-id="efde3-248">Blit Parameters</span></span>

<span data-ttu-id="efde3-249">La estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contiene parámetros generales para el blit.</span><span class="sxs-lookup"><span data-stu-id="efde3-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="efde3-250">Los parámetros más importantes se almacenan en los siguientes miembros de la estructura:</span><span class="sxs-lookup"><span data-stu-id="efde3-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="efde3-251">**TargetFrame** es el tiempo de presentación del fotograma de salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="efde3-252">En el caso del contenido progresivo, esta hora debe ser igual a la hora de inicio del fotograma actual del flujo de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="efde3-253">Esta vez se especifica en el miembro de **Inicio** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) para ese ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="efde3-254">En el caso de contenido entrelazado, un marco con dos campos intercalados genera dos fotogramas de salida desentrelazados.</span><span class="sxs-lookup"><span data-stu-id="efde3-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="efde3-255">En el primer fotograma de salida, el tiempo de presentación debe ser igual a la hora de inicio de la imagen actual en el flujo de vídeo principal, al igual que el contenido progresivo.</span><span class="sxs-lookup"><span data-stu-id="efde3-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="efde3-256">En el segundo fotograma de salida, la hora de inicio debe ser igual al punto medio entre la hora de inicio de la imagen actual en la secuencia de vídeo principal y la hora de inicio de la siguiente imagen de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="efde3-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="efde3-257">Por ejemplo, si el vídeo de entrada tiene 25 fotogramas por segundo (50 campos por segundo), los fotogramas de salida tendrán las marcas de tiempo que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="efde3-258">Las marcas de tiempo se muestran en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="efde3-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="efde3-259">Imagen de entrada</span><span class="sxs-lookup"><span data-stu-id="efde3-259">Input picture</span></span> | <span data-ttu-id="efde3-260">**TargetFrame** (1)</span><span class="sxs-lookup"><span data-stu-id="efde3-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="efde3-261">**TargetFrame** (2)</span><span class="sxs-lookup"><span data-stu-id="efde3-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="efde3-262">0</span><span class="sxs-lookup"><span data-stu-id="efde3-262">0</span></span>             | <span data-ttu-id="efde3-263">0</span><span class="sxs-lookup"><span data-stu-id="efde3-263">0</span></span>                   | <span data-ttu-id="efde3-264">200000</span><span class="sxs-lookup"><span data-stu-id="efde3-264">200000</span></span>              |
    | <span data-ttu-id="efde3-265">400000</span><span class="sxs-lookup"><span data-stu-id="efde3-265">400000</span></span>        | <span data-ttu-id="efde3-266">0</span><span class="sxs-lookup"><span data-stu-id="efde3-266">0</span></span>                   | <span data-ttu-id="efde3-267">600000</span><span class="sxs-lookup"><span data-stu-id="efde3-267">600000</span></span>              |
    | <span data-ttu-id="efde3-268">800000</span><span class="sxs-lookup"><span data-stu-id="efde3-268">800000</span></span>        | <span data-ttu-id="efde3-269">800000</span><span class="sxs-lookup"><span data-stu-id="efde3-269">800000</span></span>              | <span data-ttu-id="efde3-270">1000000</span><span class="sxs-lookup"><span data-stu-id="efde3-270">1000000</span></span>             |
    | <span data-ttu-id="efde3-271">1,2 millones</span><span class="sxs-lookup"><span data-stu-id="efde3-271">1200000</span></span>       | <span data-ttu-id="efde3-272">1,2 millones</span><span class="sxs-lookup"><span data-stu-id="efde3-272">1200000</span></span>             | <span data-ttu-id="efde3-273">1,4 millones</span><span class="sxs-lookup"><span data-stu-id="efde3-273">1400000</span></span>             |

    

     

    <span data-ttu-id="efde3-274">Si el contenido entrelazado consta de campos únicos en lugar de campos intercalados, los tiempos de salida siempre coinciden con los tiempos de entrada, como con el contenido progresivo.</span><span class="sxs-lookup"><span data-stu-id="efde3-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="efde3-275">**TargetRect** define una región rectangular dentro de la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="efde3-276">El blit escribirá la salida en esta región.</span><span class="sxs-lookup"><span data-stu-id="efde3-276">The blit will write the output to this region.</span></span> <span data-ttu-id="efde3-277">En concreto, se modificarán todos los píxeles dentro de **TargetRect** y no se modificará ningún píxel fuera de **TargetRect** .</span><span class="sxs-lookup"><span data-stu-id="efde3-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="efde3-278">El rectángulo de destino define el rectángulo delimitador de todas las secuencias de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="efde3-279">La colocación de flujos individuales dentro de ese rectángulo se controla mediante el parámetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="efde3-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="efde3-280">**BackgroundColor** proporciona el color del fondo siempre que no aparezca ninguna imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="efde3-281">Por ejemplo, cuando se muestra una imagen de 16 x 9 en una superficie de 4 x 3 (panorámica), se muestran las regiones con el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="efde3-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="efde3-282">El color de fondo solo se aplica dentro del rectángulo de destino (**TargetRect**).</span><span class="sxs-lookup"><span data-stu-id="efde3-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="efde3-283">Los píxeles fuera de **TargetRect** no se modifican.</span><span class="sxs-lookup"><span data-stu-id="efde3-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="efde3-284">**DestFormat** describe el espacio de colores del vídeo de salida, por ejemplo, si se usa el color ITU-R BT. 709 o BT. 601.</span><span class="sxs-lookup"><span data-stu-id="efde3-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="efde3-285">Esta información puede afectar al modo en que se muestra la imagen.</span><span class="sxs-lookup"><span data-stu-id="efde3-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="efde3-286">Para obtener más información, vea [información de color extendido](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="efde3-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="efde3-287">Otros parámetros se describen en la página de referencia de la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="efde3-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="efde3-288">Ejemplos de entrada</span><span class="sxs-lookup"><span data-stu-id="efde3-288">Input Samples</span></span>

<span data-ttu-id="efde3-289">El parámetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) apunta a una matriz de estructuras de [**\_ videoejemplo de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="efde3-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="efde3-290">Cada una de estas estructuras contiene información sobre un ejemplo de entrada y un puntero a la superficie de Direct3D que contiene el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="efde3-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="efde3-291">Cada ejemplo es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="efde3-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="efde3-292">La imagen actual del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="efde3-293">Una imagen de referencia hacia delante o hacia atrás desde el flujo principal, que se usa para Desentrelazar.</span><span class="sxs-lookup"><span data-stu-id="efde3-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="efde3-294">Imagen de subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="efde3-294">A substream picture.</span></span>

<span data-ttu-id="efde3-295">El orden exacto en el que las muestras deben aparecer en la matriz se describe más adelante, en la sección [orden de ejemplo de entrada](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="efde3-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="efde3-296">Se pueden proporcionar hasta 15 imágenes de subflujo, aunque la mayoría de las aplicaciones de vídeo solo necesitan un subflujo, como máximo.</span><span class="sxs-lookup"><span data-stu-id="efde3-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="efde3-297">El número de subsecuencias puede cambiar con cada llamada a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="efde3-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="efde3-298">Las imágenes de subflujo se indican estableciendo el miembro **SampleFormat. SampleFormat** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) igual a DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="efde3-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="efde3-299">En el flujo de vídeo principal, este miembro describe el entrelazado del vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="efde3-300">Para obtener más información, consulte enumeración [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) .</span><span class="sxs-lookup"><span data-stu-id="efde3-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="efde3-301">En el flujo de vídeo principal, los miembros **inicial** y **final** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) proporcionan las horas de inicio y finalización de la muestra de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="efde3-302">En el caso de las imágenes de subflujo, establezca estos valores en cero, ya que el tiempo de presentación siempre se calcula a partir del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="efde3-303">La aplicación es responsable del seguimiento cuando se debe presentar cada imagen de subflujo y enviarla a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="efde3-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="efde3-304">Dos rectángulos definen cómo se coloca el vídeo de origen para cada flujo:</span><span class="sxs-lookup"><span data-stu-id="efde3-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="efde3-305">El miembro **SrcRect** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) especifica el *rectángulo de origen*, una región rectangular de la imagen de origen que aparecerá en el marco de salida compuesto.</span><span class="sxs-lookup"><span data-stu-id="efde3-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="efde3-306">Para recortar la imagen, establézcalo en un valor menor que el tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="efde3-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="efde3-307">En caso contrario, establézcalo igual al tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="efde3-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="efde3-308">El miembro **DstRect** de la misma estructura especifica el *rectángulo de destino*, una región rectangular de la superficie de destino donde aparecerá el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="efde3-309">El controlador blits píxeles desde el rectángulo de origen al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="efde3-310">Los dos rectángulos pueden tener diferentes tamaños o relaciones de aspecto. el controlador escalará la imagen según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="efde3-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="efde3-311">Además, cada flujo de entrada puede usar un factor de escala diferente.</span><span class="sxs-lookup"><span data-stu-id="efde3-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="efde3-312">De hecho, es posible que sea necesario escalar para generar la relación de aspecto correcta en el marco de salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="efde3-313">El controlador no tiene en cuenta la proporción de aspecto de píxeles del origen, por lo que si la imagen de origen usa píxeles no cuadrados, depende de la aplicación calcular el rectángulo de destino correcto.</span><span class="sxs-lookup"><span data-stu-id="efde3-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="efde3-314">Los formatos de subflujo preferidos son AYUV y AI44.</span><span class="sxs-lookup"><span data-stu-id="efde3-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="efde3-315">El último es un formato de paleta con 16 colores.</span><span class="sxs-lookup"><span data-stu-id="efde3-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="efde3-316">Las entradas de la paleta se especifican en el miembro **PAL** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="efde3-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="efde3-317">(Si el formato de vídeo de origen se expresa originalmente como Media Foundation tipo de medio, las entradas de la paleta se almacenan en el atributo [**MF \_ MT \_ Palette**](mf-mt-palette-attribute.md) ). En el caso de los formatos no de paleta, borre esta matriz en cero.</span><span class="sxs-lookup"><span data-stu-id="efde3-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="efde3-318">Composición de imagen</span><span class="sxs-lookup"><span data-stu-id="efde3-318">Image Composition</span></span>

<span data-ttu-id="efde3-319">Cada operación de blit se define mediante los tres rectángulos siguientes:</span><span class="sxs-lookup"><span data-stu-id="efde3-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="efde3-320">El rectángulo de *destino* (**TargetRect**) define la región dentro de la superficie de destino en la que aparecerá la salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="efde3-321">La imagen de salida se recorta a este rectángulo.</span><span class="sxs-lookup"><span data-stu-id="efde3-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="efde3-322">El rectángulo de *destino* de cada secuencia (**DstRect**) define dónde aparece el flujo de entrada en la imagen compuesta.</span><span class="sxs-lookup"><span data-stu-id="efde3-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="efde3-323">El rectángulo de *origen* de cada flujo (**SrcRect**) define qué parte de la imagen de origen aparece.</span><span class="sxs-lookup"><span data-stu-id="efde3-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="efde3-324">Los rectángulos de destino y destino se especifican en relación con la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="efde3-325">El rectángulo de origen se especifica en relación con la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="efde3-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="efde3-326">Todos los rectángulos se especifican en píxeles.</span><span class="sxs-lookup"><span data-stu-id="efde3-326">All rectangles are specified in pixels.</span></span>

![diagrama que muestra los rectángulos de origen, destino y destino](images/dxva-vp-rects.gif)

<span data-ttu-id="efde3-328">El dispositivo de procesamiento de vídeo alfa combina las imágenes de entrada con cualquiera de los siguientes orígenes de datos alfa:</span><span class="sxs-lookup"><span data-stu-id="efde3-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="efde3-329">Datos alfa por píxel de subsecuencias.</span><span class="sxs-lookup"><span data-stu-id="efde3-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="efde3-330">Un valor alfa plano para cada flujo de vídeo, especificado en el miembro **PlanarAlpha** de la estructura de [**\_ videoejemplo DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="efde3-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="efde3-331">Valor alfa plano de la imagen compuesta, especificado en el miembro **alfa** de la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="efde3-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="efde3-332">Este valor se usa para fusionar toda la imagen compuesta con el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="efde3-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="efde3-333">En esta sección se proporciona una serie de ejemplos que muestran cómo el dispositivo de procesamiento de vídeo crea la imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="efde3-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="efde3-334">Ejemplo 1: panorámica</span><span class="sxs-lookup"><span data-stu-id="efde3-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="efde3-335">En este ejemplo se muestra cómo aplicar una panorámica a la imagen de origen, estableciendo el rectángulo de destino para que sea menor que el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="efde3-336">La secuencia de vídeo principal de este ejemplo es una imagen 720 × 480 y está pensada para mostrarse con una relación de aspecto de 16:9.</span><span class="sxs-lookup"><span data-stu-id="efde3-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="efde3-337">La superficie de destino es 640 × 480 píxeles (relación de aspecto de 4:3).</span><span class="sxs-lookup"><span data-stu-id="efde3-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="efde3-338">Para lograr la relación de aspecto correcta, el rectángulo de destino debe ser 640 × 360.</span><span class="sxs-lookup"><span data-stu-id="efde3-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="efde3-339">Para simplificar, en este ejemplo no se incluye un subflujo.</span><span class="sxs-lookup"><span data-stu-id="efde3-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="efde3-340">En el diagrama siguiente se muestran los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-340">The following diagram shows the source and destination rectangles.</span></span>

![diagrama que muestra la panorámica.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="efde3-342">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-343">Rectángulo de destino: {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="efde3-344">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-344">Primary video:</span></span>

    -   <span data-ttu-id="efde3-345">Rectángulo de origen: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-346">Rectángulo de destino: {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="efde3-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="efde3-347">El controlador desentrelazará el vídeo, reducirá el fotograma desentrelazado a 640 × 360 y convertirá el marco en el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="efde3-348">El rectángulo de destino es mayor que el rectángulo de destino, por lo que el controlador usará el color de fondo para rellenar las barras horizontales por encima y por debajo del marco.</span><span class="sxs-lookup"><span data-stu-id="efde3-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="efde3-349">El color de fondo se especifica en la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="efde3-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="efde3-350">Ejemplo 2: expandir imágenes de subflujo</span><span class="sxs-lookup"><span data-stu-id="efde3-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="efde3-351">Las imágenes de subflujo pueden extenderse más allá de la imagen de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="efde3-352">En vídeo DVD, por ejemplo, la secuencia de vídeo principal puede tener una relación de aspecto 4:3 mientras que la subsecuencia es 16:9.</span><span class="sxs-lookup"><span data-stu-id="efde3-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="efde3-353">En este ejemplo, ambos flujos de vídeo tienen las mismas dimensiones de origen (720 × 480), pero el subflujo está diseñado para mostrarse en una relación de aspecto de 16:9.</span><span class="sxs-lookup"><span data-stu-id="efde3-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="efde3-354">Para lograr esta relación de aspecto, la imagen de subflujo se estira horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="efde3-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="efde3-355">Los rectángulos de origen y de destino se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-355">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama que muestra el ajuste de imagen de subflujo.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="efde3-357">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-358">Rectángulo de destino: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="efde3-359">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-359">Primary video:</span></span>

    -   <span data-ttu-id="efde3-360">Rectángulo de origen: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-361">Rectángulo de destino: {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="efde3-362">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-362">Substream:</span></span>
    -   <span data-ttu-id="efde3-363">Rectángulo de origen: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-364">Rectángulo de destino: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="efde3-365">Estos valores conservan el alto de la imagen y escalan ambas imágenes horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="efde3-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="efde3-366">En las regiones en las que aparecen ambas imágenes, se combinan alfa.</span><span class="sxs-lookup"><span data-stu-id="efde3-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="efde3-367">En el caso de que la imagen de subflujo se desacabe más allá del vídeo de la ubicación, el subflujo se mezcla alfa con el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="efde3-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="efde3-368">Esta mezcla alfa cuenta con los colores modificados en el lado derecho del diagrama.</span><span class="sxs-lookup"><span data-stu-id="efde3-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="efde3-369">Ejemplo 3: alto de flujo no coincidente</span><span class="sxs-lookup"><span data-stu-id="efde3-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="efde3-370">En el ejemplo anterior, la subsecuencia y el flujo principal tienen el mismo alto.</span><span class="sxs-lookup"><span data-stu-id="efde3-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="efde3-371">Los flujos también pueden tener un alto no coincidente, tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="efde3-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="efde3-372">Las áreas del rectángulo de destino donde no aparece ningún vídeo se dibujan con el color de fondo, en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="efde3-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="efde3-373">Los rectángulos de origen y de destino se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-373">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama que muestra el alto de los flujos no coincidentes,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="efde3-375">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-376">Rectángulo de destino: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="efde3-377">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-377">Primary video:</span></span>
    -   <span data-ttu-id="efde3-378">Rectángulo de origen: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="efde3-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="efde3-379">Rectángulo de destino: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="efde3-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="efde3-380">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-380">Substream:</span></span>
    -   <span data-ttu-id="efde3-381">Rectángulo de origen: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="efde3-382">Rectángulo de destino: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="efde3-383">Ejemplo 4: rectángulo de destino menor que la superficie de destino</span><span class="sxs-lookup"><span data-stu-id="efde3-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="efde3-384">Este ejemplo muestra un caso en el que el rectángulo de destino es menor que la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![diagrama que muestra un blit a un rectángulo de destino.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="efde3-386">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-387">Superficie de destino: {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="efde3-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="efde3-388">Rectángulo de destino: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="efde3-389">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-389">Primary video:</span></span>
    -   <span data-ttu-id="efde3-390">Rectángulo de origen: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="efde3-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="efde3-391">Rectángulo de destino: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="efde3-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="efde3-392">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-392">Substream:</span></span>
    -   <span data-ttu-id="efde3-393">Rectángulo de origen: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="efde3-394">Rectángulo de destino: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="efde3-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="efde3-395">Los píxeles que están fuera del rectángulo de destino no se modifican, por lo que el color de fondo solo aparece dentro del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="efde3-396">El área de puntos indica partes de la superficie de destino que no se ven afectadas por el blit.</span><span class="sxs-lookup"><span data-stu-id="efde3-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="efde3-397">Ejemplo 5: rectángulos de origen</span><span class="sxs-lookup"><span data-stu-id="efde3-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="efde3-398">Si especifica un rectángulo de origen menor que el de la imagen de origen, el controlador convertirá solo esa parte de la imagen.</span><span class="sxs-lookup"><span data-stu-id="efde3-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="efde3-399">En este ejemplo, los rectángulos de origen especifican el cuadrante inferior derecho de la secuencia de vídeo principal y el cuadrante inferior izquierdo de la subsecuencia (indicado por marcas de hash en el diagrama).</span><span class="sxs-lookup"><span data-stu-id="efde3-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="efde3-400">Los rectángulos de destino tienen el mismo tamaño que los rectángulos de origen, por lo que el vídeo no se ajusta.</span><span class="sxs-lookup"><span data-stu-id="efde3-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="efde3-401">Los rectángulos de origen y de destino se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-401">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama que muestra un blit de dos rectángulos de origen.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="efde3-403">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-404">Rectángulo de destino: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="efde3-405">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-405">Primary video:</span></span>
    -   <span data-ttu-id="efde3-406">Tamaño de la superficie de origen: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-407">Rectángulo de origen: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-408">Rectángulo de destino: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="efde3-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="efde3-409">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-409">Substream:</span></span>
    -   <span data-ttu-id="efde3-410">Tamaño de la superficie de origen: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="efde3-411">Rectángulo de origen: {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="efde3-412">Rectángulo de destino: {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="efde3-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="efde3-413">Ejemplo 6: intersección de rectángulos de destino</span><span class="sxs-lookup"><span data-stu-id="efde3-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="efde3-414">Este ejemplo es similar al anterior, pero los rectángulos de destino forman una intersección.</span><span class="sxs-lookup"><span data-stu-id="efde3-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="efde3-415">Las dimensiones de la superficie son las mismas que en el ejemplo anterior, pero los rectángulos de origen y de destino no.</span><span class="sxs-lookup"><span data-stu-id="efde3-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="efde3-416">De nuevo, el vídeo se recorta pero no se ajusta.</span><span class="sxs-lookup"><span data-stu-id="efde3-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="efde3-417">Los rectángulos de origen y de destino se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-417">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama que muestra los rectángulos de destino de intersección.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="efde3-419">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-420">Rectángulo de destino: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="efde3-421">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-421">Primary video:</span></span>
    -   <span data-ttu-id="efde3-422">Tamaño de la superficie de origen: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-423">Rectángulo de origen: {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="efde3-424">Rectángulo de destino: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="efde3-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="efde3-425">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-425">Substream:</span></span>
    -   <span data-ttu-id="efde3-426">Tamaño de la superficie de origen: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="efde3-427">Rectángulo de origen: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="efde3-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="efde3-428">Rectángulo de destino: {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="efde3-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="efde3-429">Ejemplo 7: expandir y recortar vídeo</span><span class="sxs-lookup"><span data-stu-id="efde3-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="efde3-430">En este ejemplo, el vídeo se estira y se recorta.</span><span class="sxs-lookup"><span data-stu-id="efde3-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="efde3-431">Una región 180 × 120 de cada flujo se expande para abarcar un área de 360 × 240 en el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="efde3-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![diagrama que muestra la expansión y el recorte.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="efde3-433">En el diagrama anterior se muestran los siguientes rectángulos:</span><span class="sxs-lookup"><span data-stu-id="efde3-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="efde3-434">Rectángulo de destino: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="efde3-435">Vídeo principal:</span><span class="sxs-lookup"><span data-stu-id="efde3-435">Primary video:</span></span>
    -   <span data-ttu-id="efde3-436">Tamaño de la superficie de origen: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="efde3-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="efde3-437">Rectángulo de origen: {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="efde3-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="efde3-438">Rectángulo de destino: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="efde3-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="efde3-439">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-439">Substream:</span></span>
    -   <span data-ttu-id="efde3-440">Tamaño de la superficie de origen: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="efde3-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="efde3-441">Rectángulo de origen: {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="efde3-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="efde3-442">Rectángulo de destino: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="efde3-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="efde3-443">Orden de ejemplo de entrada</span><span class="sxs-lookup"><span data-stu-id="efde3-443">Input Sample Order</span></span>

<span data-ttu-id="efde3-444">El parámetro *pSamples* del método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) es un puntero a una matriz de ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="efde3-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="efde3-445">Los ejemplos del flujo de vídeo principal aparecen en primer lugar, seguidos de las imágenes de subsecuencia en orden Z.</span><span class="sxs-lookup"><span data-stu-id="efde3-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="efde3-446">Los ejemplos se deben colocar en la matriz en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="efde3-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="efde3-447">Los ejemplos de la secuencia de vídeo principal aparecen en primer lugar en la matriz, en orden temporal.</span><span class="sxs-lookup"><span data-stu-id="efde3-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="efde3-448">Dependiendo del modo de desentrelazado, el controlador puede requerir uno o más ejemplos de referencia de la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="efde3-449">Los miembros **NumForwardRefSamples** y **NumBackwardRefSamples** de la estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) especifican el número de ejemplos de referencia hacia delante y hacia atrás que son necesarios.</span><span class="sxs-lookup"><span data-stu-id="efde3-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="efde3-450">El autor de la llamada debe proporcionar estos ejemplos de referencia incluso si el contenido del vídeo es progresivo y no requiere desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="efde3-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="efde3-451">(Esto puede ocurrir cuando se proporcionan fotogramas progresivos a un dispositivo de desentrelazado, por ejemplo, cuando el origen contiene una mezcla de fotogramas entrelazados y progresivos).</span><span class="sxs-lookup"><span data-stu-id="efde3-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="efde3-452">Después de los ejemplos de la secuencia de vídeo principal, la matriz puede contener hasta 15 muestras de subflujo, organizadas en orden Z, de abajo a arriba.</span><span class="sxs-lookup"><span data-stu-id="efde3-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="efde3-453">Las subsecuencias siempre son progresivas y no requieren imágenes de referencia.</span><span class="sxs-lookup"><span data-stu-id="efde3-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="efde3-454">En cualquier momento, la secuencia de vídeo principal puede cambiar entre el contenido entrelazado y progresivo, y el número de subflujos puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="efde3-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="efde3-455">El miembro **SampleFormat. SampleFormat** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica el tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="efde3-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="efde3-456">En el caso de las imágenes de subflujo, establezca este valor en DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="efde3-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="efde3-457">En el caso de las imágenes progresivas, el valor es DXVA2 \_ SampleProgressiveFrame.</span><span class="sxs-lookup"><span data-stu-id="efde3-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="efde3-458">En el caso de las imágenes entrelazadas, el valor depende del diseño del campo.</span><span class="sxs-lookup"><span data-stu-id="efde3-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="efde3-459">Si el controlador requiere ejemplos de referencia hacia delante y hacia atrás, es posible que el número total de muestras no esté disponible al principio de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="efde3-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="efde3-460">En ese caso, incluya entradas para ellos en la matriz *pSamples* , pero marque los ejemplos que faltan como si tuvieran el tipo DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="efde3-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="efde3-461">Los miembros **inicial** y **final** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) proporcionan la ubicación temporal de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="efde3-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="efde3-462">Estos valores solo se usan para los ejemplos de la secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="efde3-463">En el caso de las imágenes de subflujo, establezca ambos miembros en cero.</span><span class="sxs-lookup"><span data-stu-id="efde3-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="efde3-464">Los ejemplos siguientes pueden ayudarle a aclarar estos requisitos.</span><span class="sxs-lookup"><span data-stu-id="efde3-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="efde3-465">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="efde3-465">Example 1</span></span>

<span data-ttu-id="efde3-466">El caso más simple se produce cuando no hay subsecuencias y el algoritmo de desentrelazado no requiere ejemplos de referencia (**NumForwardRefSamples** y **NumBackwardRefSamples** son cero).</span><span class="sxs-lookup"><span data-stu-id="efde3-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="efde3-467">Bob desentrelazado es un ejemplo de este tipo de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="efde3-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="efde3-468">En este caso, la matriz *pSamples* debe contener una sola superficie de entrada, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="efde3-469">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-469">Index</span></span>           | <span data-ttu-id="efde3-470">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-470">Surface type</span></span>        | <span data-ttu-id="efde3-471">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="efde3-472">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-473">Imagen entrelazada.</span><span class="sxs-lookup"><span data-stu-id="efde3-473">Interlaced picture.</span></span> | <span data-ttu-id="efde3-474">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-474">*T*</span></span>               |



 

<span data-ttu-id="efde3-475">Se supone que el valor de hora *T* es la hora de inicio del fotograma de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="efde3-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="efde3-476">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="efde3-476">Example 2</span></span>

<span data-ttu-id="efde3-477">En este ejemplo, la aplicación mezcla dos subsecuencias con el flujo principal.</span><span class="sxs-lookup"><span data-stu-id="efde3-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="efde3-478">El algoritmo de desentrelazado no requiere ejemplos de referencia.</span><span class="sxs-lookup"><span data-stu-id="efde3-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="efde3-479">En la tabla siguiente se muestra cómo se organizan estos ejemplos en la matriz *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="efde3-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="efde3-480">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-480">Index</span></span>           | <span data-ttu-id="efde3-481">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-481">Surface type</span></span>       | <span data-ttu-id="efde3-482">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-482">Temporal location</span></span> | <span data-ttu-id="efde3-483">Orden Z</span><span class="sxs-lookup"><span data-stu-id="efde3-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="efde3-484">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-485">Imagen entrelazada</span><span class="sxs-lookup"><span data-stu-id="efde3-485">Interlaced picture</span></span> | <span data-ttu-id="efde3-486">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-486">*T*</span></span>               | <span data-ttu-id="efde3-487">0</span><span class="sxs-lookup"><span data-stu-id="efde3-487">0</span></span>       |
| <span data-ttu-id="efde3-488">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-489">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-489">Substream</span></span>          | <span data-ttu-id="efde3-490">0</span><span class="sxs-lookup"><span data-stu-id="efde3-490">0</span></span>                 | <span data-ttu-id="efde3-491">1</span><span class="sxs-lookup"><span data-stu-id="efde3-491">1</span></span>       |
| <span data-ttu-id="efde3-492">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-493">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-493">Substream</span></span>          | <span data-ttu-id="efde3-494">0</span><span class="sxs-lookup"><span data-stu-id="efde3-494">0</span></span>                 | <span data-ttu-id="efde3-495">2</span><span class="sxs-lookup"><span data-stu-id="efde3-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="efde3-496">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="efde3-496">Example 3</span></span>

<span data-ttu-id="efde3-497">Ahora Supongamos que el algoritmo de desentrelazado requiere un ejemplo de referencia inversa y un ejemplo de referencia adelantada.</span><span class="sxs-lookup"><span data-stu-id="efde3-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="efde3-498">Además, se proporcionan dos imágenes de subflujo, para un total de cinco superficies.</span><span class="sxs-lookup"><span data-stu-id="efde3-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="efde3-499">En la tabla siguiente se muestra el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="efde3-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="efde3-500">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-500">Index</span></span>           | <span data-ttu-id="efde3-501">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-501">Surface type</span></span>                   | <span data-ttu-id="efde3-502">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-502">Temporal location</span></span> | <span data-ttu-id="efde3-503">Orden Z</span><span class="sxs-lookup"><span data-stu-id="efde3-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="efde3-504">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-505">Imagen entrelazada (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="efde3-506">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="efde3-506">*T* −1</span></span>            | <span data-ttu-id="efde3-507">No aplicable</span><span class="sxs-lookup"><span data-stu-id="efde3-507">Not applicable</span></span> |
| <span data-ttu-id="efde3-508">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-509">Imagen entrelazada</span><span class="sxs-lookup"><span data-stu-id="efde3-509">Interlaced picture</span></span>             | <span data-ttu-id="efde3-510">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-510">*T*</span></span>               | <span data-ttu-id="efde3-511">0</span><span class="sxs-lookup"><span data-stu-id="efde3-511">0</span></span>              |
| <span data-ttu-id="efde3-512">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-513">Imagen entrelazada (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="efde3-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="efde3-514">*T* +1</span></span>            | <span data-ttu-id="efde3-515">No aplicable</span><span class="sxs-lookup"><span data-stu-id="efde3-515">Not applicable</span></span> |
| <span data-ttu-id="efde3-516">*pSamples* \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="efde3-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="efde3-517">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-517">Substream</span></span>                      | <span data-ttu-id="efde3-518">0</span><span class="sxs-lookup"><span data-stu-id="efde3-518">0</span></span>                 | <span data-ttu-id="efde3-519">1</span><span class="sxs-lookup"><span data-stu-id="efde3-519">1</span></span>              |
| <span data-ttu-id="efde3-520">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="efde3-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="efde3-521">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-521">Substream</span></span>                      | <span data-ttu-id="efde3-522">0</span><span class="sxs-lookup"><span data-stu-id="efde3-522">0</span></span>                 | <span data-ttu-id="efde3-523">2</span><span class="sxs-lookup"><span data-stu-id="efde3-523">2</span></span>              |



 

<span data-ttu-id="efde3-524">El tiempo *T* − 1 es la hora de inicio del fotograma anterior al marco actual y *T* + 1 es la hora de inicio del siguiente fotograma.</span><span class="sxs-lookup"><span data-stu-id="efde3-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="efde3-525">Si la secuencia de vídeo cambia a contenido progresivo, utilizando el mismo modo de desentrelazado, la aplicación debe proporcionar el mismo número de ejemplos, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="efde3-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="efde3-526">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-526">Index</span></span>           | <span data-ttu-id="efde3-527">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-527">Surface type</span></span>                    | <span data-ttu-id="efde3-528">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-528">Temporal location</span></span> | <span data-ttu-id="efde3-529">Orden Z</span><span class="sxs-lookup"><span data-stu-id="efde3-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="efde3-530">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-531">Imagen progresiva (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-531">Progressive picture (reference)</span></span> | <span data-ttu-id="efde3-532">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="efde3-532">*T* −1</span></span>            | <span data-ttu-id="efde3-533">No aplicable</span><span class="sxs-lookup"><span data-stu-id="efde3-533">Not applicable</span></span> |
| <span data-ttu-id="efde3-534">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-535">Imagen progresiva</span><span class="sxs-lookup"><span data-stu-id="efde3-535">Progressive picture</span></span>             | <span data-ttu-id="efde3-536">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-536">*T*</span></span>               | <span data-ttu-id="efde3-537">0</span><span class="sxs-lookup"><span data-stu-id="efde3-537">0</span></span>              |
| <span data-ttu-id="efde3-538">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-539">Imagen progresiva (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-539">Progressive picture (reference)</span></span> | <span data-ttu-id="efde3-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="efde3-540">*T* +1</span></span>            | <span data-ttu-id="efde3-541">No aplicable</span><span class="sxs-lookup"><span data-stu-id="efde3-541">Not applicable</span></span> |
| <span data-ttu-id="efde3-542">*pSamples* \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="efde3-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="efde3-543">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-543">Substream</span></span>                       | <span data-ttu-id="efde3-544">0</span><span class="sxs-lookup"><span data-stu-id="efde3-544">0</span></span>                 | <span data-ttu-id="efde3-545">1</span><span class="sxs-lookup"><span data-stu-id="efde3-545">1</span></span>              |
| <span data-ttu-id="efde3-546">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="efde3-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="efde3-547">Subtransmisiones</span><span class="sxs-lookup"><span data-stu-id="efde3-547">Substream</span></span>                       | <span data-ttu-id="efde3-548">0</span><span class="sxs-lookup"><span data-stu-id="efde3-548">0</span></span>                 | <span data-ttu-id="efde3-549">2</span><span class="sxs-lookup"><span data-stu-id="efde3-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="efde3-550">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="efde3-550">Example 4</span></span>

<span data-ttu-id="efde3-551">Al principio de una secuencia de vídeo, es posible que los ejemplos de referencia hacia delante y hacia atrás no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="efde3-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="efde3-552">Cuando esto sucede, las entradas de los ejemplos que faltan se incluyen en la matriz *pSamples* , con el tipo de ejemplo DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="efde3-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="efde3-553">Suponiendo que el modo de desentrelazado necesita una muestra de referencia hacia delante y una de referencias inversas, las tres primeras llamadas a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) tendrían las secuencias de entradas que se muestran en las tres tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="efde3-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="efde3-554">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-554">Index</span></span>           | <span data-ttu-id="efde3-555">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-555">Surface type</span></span>                   | <span data-ttu-id="efde3-556">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="efde3-557">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-558">Unknown</span><span class="sxs-lookup"><span data-stu-id="efde3-558">Unknown</span></span>                        | <span data-ttu-id="efde3-559">0</span><span class="sxs-lookup"><span data-stu-id="efde3-559">0</span></span>                 |
| <span data-ttu-id="efde3-560">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-561">Unknown</span><span class="sxs-lookup"><span data-stu-id="efde3-561">Unknown</span></span>                        | <span data-ttu-id="efde3-562">0</span><span class="sxs-lookup"><span data-stu-id="efde3-562">0</span></span>                 |
| <span data-ttu-id="efde3-563">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-564">Imagen entrelazada (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="efde3-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="efde3-565">*T* +1</span></span>            |



 



| <span data-ttu-id="efde3-566">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-566">Index</span></span>           | <span data-ttu-id="efde3-567">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-567">Surface type</span></span>                   | <span data-ttu-id="efde3-568">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="efde3-569">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-570">Unknown</span><span class="sxs-lookup"><span data-stu-id="efde3-570">Unknown</span></span>                        | <span data-ttu-id="efde3-571">0</span><span class="sxs-lookup"><span data-stu-id="efde3-571">0</span></span>                 |
| <span data-ttu-id="efde3-572">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-573">Imagen entrelazada</span><span class="sxs-lookup"><span data-stu-id="efde3-573">Interlaced picture</span></span>             | <span data-ttu-id="efde3-574">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-574">*T*</span></span>               |
| <span data-ttu-id="efde3-575">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-576">Imagen entrelazada (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="efde3-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="efde3-577">*T* +1</span></span>            |



 



| <span data-ttu-id="efde3-578">Índice</span><span class="sxs-lookup"><span data-stu-id="efde3-578">Index</span></span>           | <span data-ttu-id="efde3-579">Tipo de superficie</span><span class="sxs-lookup"><span data-stu-id="efde3-579">Surface type</span></span>                   | <span data-ttu-id="efde3-580">Ubicación temporal</span><span class="sxs-lookup"><span data-stu-id="efde3-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="efde3-581">*pSamples* \[ 0,1\]</span><span class="sxs-lookup"><span data-stu-id="efde3-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="efde3-582">Imagen entrelazada</span><span class="sxs-lookup"><span data-stu-id="efde3-582">Interlaced picture</span></span>             | <span data-ttu-id="efde3-583">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="efde3-583">*T* −1</span></span>            |
| <span data-ttu-id="efde3-584">*pSamples* \[ dimensional\]</span><span class="sxs-lookup"><span data-stu-id="efde3-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="efde3-585">Imagen entrelazada</span><span class="sxs-lookup"><span data-stu-id="efde3-585">Interlaced picture</span></span>             | <span data-ttu-id="efde3-586">*T*</span><span class="sxs-lookup"><span data-stu-id="efde3-586">*T*</span></span>               |
| <span data-ttu-id="efde3-587">*pSamples* \[ dos\]</span><span class="sxs-lookup"><span data-stu-id="efde3-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="efde3-588">Imagen entrelazada (referencia)</span><span class="sxs-lookup"><span data-stu-id="efde3-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="efde3-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="efde3-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="efde3-590">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efde3-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efde3-591">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="efde3-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="efde3-592">DXVA2 \_ ejemplo de Videoproc</span><span class="sxs-lookup"><span data-stu-id="efde3-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
