---
description: En este tema se ofrece información general sobre las API de codificación de archivos que se proporcionan en Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Información general de la codificación en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104552529"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="f93ae-103">Información general de la codificación en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f93ae-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="f93ae-104">En este tema se ofrece información general sobre las API de codificación de archivos que se proporcionan en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f93ae-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="f93ae-105">Terminología</span><span class="sxs-lookup"><span data-stu-id="f93ae-105">Terminology</span></span>

<span data-ttu-id="f93ae-106">La *codificación* es un término general que abarca varios procesos distintos:</span><span class="sxs-lookup"><span data-stu-id="f93ae-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="f93ae-107">Codificar una secuencia de audio o vídeo en formatos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="f93ae-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="f93ae-108">Por ejemplo, codificar una secuencia de vídeo en un vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="f93ae-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="f93ae-109">Multiplexación ("Multiplexación") uno o más flujos en una sola secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="f93ae-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="f93ae-110">Normalmente, los flujos entrantes se codifican en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="f93ae-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="f93ae-111">Este paso puede implicar la packetabilidad de las secuencias codificadas.</span><span class="sxs-lookup"><span data-stu-id="f93ae-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="f93ae-112">Escritura de una secuencia de bytes multiplexada en un archivo, como un archivo MP4 o Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="f93ae-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="f93ae-113">Como alternativa, la secuencia multiplexada se puede enviar a través de la red.</span><span class="sxs-lookup"><span data-stu-id="f93ae-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="f93ae-114">En el diagrama siguiente se muestran estos tres procesos:</span><span class="sxs-lookup"><span data-stu-id="f93ae-114">The following diagram shows these three processes:</span></span>

![diagrama que muestra los procesos de codificación y multiplexación](images/encoding03.png)

<span data-ttu-id="f93ae-116">Entre las variaciones de este proceso se incluyen transcodificación y remuxing:</span><span class="sxs-lookup"><span data-stu-id="f93ae-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="f93ae-117">La *transcodificación* significa descodificar un archivo existente, volver a codificar los flujos y volver a multiplexar las secuencias codificadas.</span><span class="sxs-lookup"><span data-stu-id="f93ae-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="f93ae-118">La transcodificación puede realizarse para convertir un archivo de un tipo de codificación a otro; por ejemplo, para convertir el vídeo H. 264 en Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="f93ae-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="f93ae-119">También se puede hacer para cambiar la velocidad de bits codificada; tamaño del fotograma de vídeo; la velocidad de fotogramas; u otros parámetros de formato.</span><span class="sxs-lookup"><span data-stu-id="f93ae-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="f93ae-120">*Remultiplexar* o *remuxing* significa desmultiplexar un archivo y volver a multiplexar los flujos, sin ningún paso de descodificación/codificación.</span><span class="sxs-lookup"><span data-stu-id="f93ae-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="f93ae-121">Esto puede hacerse para cambiar el modo en que los paquetes de audio y vídeo se multiplexan, para quitar una secuencia o para combinar secuencias de dos archivos de origen diferentes.</span><span class="sxs-lookup"><span data-stu-id="f93ae-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="f93ae-122">*Transclasificación* es un caso especial de transcodificación, donde se cambia la velocidad de bits sin cambiar el tipo de compresión.</span><span class="sxs-lookup"><span data-stu-id="f93ae-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="f93ae-123">Por ejemplo, puede convertir un archivo de velocidad de bits alto en una velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="f93ae-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="f93ae-124">Un escenario típico en el que se podría usar la transclasificación es al sincronizar contenido multimedia desde un equipo a un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="f93ae-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="f93ae-125">Si el dispositivo portátil no es compatible con una velocidad de bits alta, el archivo se puede transclasificar antes de copiarlo en el dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="f93ae-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="f93ae-126">El siguiente diagrama de bloque muestra el proceso de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="f93ae-126">The following block diagram shows the transcoding process.</span></span>

![diagrama que muestra el proceso de transcodificación](images/encoding05.png)

<span data-ttu-id="f93ae-128">El siguiente diagrama de bloque muestra el proceso remuxing.</span><span class="sxs-lookup"><span data-stu-id="f93ae-128">The following block diagram shows the remuxing process.</span></span>

![diagrama que muestra el proceso remuxing](images/encoding06.png)

<span data-ttu-id="f93ae-130">En ocasiones, en esta documentación se usa la *codificación* de términos para incluir transcodificación y remuxing.</span><span class="sxs-lookup"><span data-stu-id="f93ae-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="f93ae-131">Cuando sea importante distinguir entre ellos, la documentación indicará la diferencia.</span><span class="sxs-lookup"><span data-stu-id="f93ae-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="f93ae-132">Vea también: [Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="f93ae-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="f93ae-133">Arquitectura de codificación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f93ae-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="f93ae-134">En el nivel más bajo de la arquitectura de Media Foundation, se usan los siguientes tipos de componente para la codificación:</span><span class="sxs-lookup"><span data-stu-id="f93ae-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="f93ae-135">Para la transcodificación, los [orígenes multimedia](media-sources.md) se usan para desmultiplexar el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="f93ae-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="f93ae-136">En el proceso de codificación, se usan [Media Foundation transformaciones](media-foundation-transforms.md) para descodificar y codificar secuencias.</span><span class="sxs-lookup"><span data-stu-id="f93ae-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="f93ae-137">En el proceso de multiplexación, los [receptores de medios](media-sinks.md) se usan para multiplexar los flujos y escribir la secuencia multiplexada en un archivo o una red.</span><span class="sxs-lookup"><span data-stu-id="f93ae-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="f93ae-138">En el siguiente diagrama se muestra el flujo de datos entre estos componentes en un escenario de transcodificación:</span><span class="sxs-lookup"><span data-stu-id="f93ae-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![diagrama que muestra los componentes usados en la transcodificación](images/encoding04.png)

<span data-ttu-id="f93ae-140">La mayoría de las aplicaciones no usarán estos componentes directamente.</span><span class="sxs-lookup"><span data-stu-id="f93ae-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="f93ae-141">En su lugar, una aplicación usará API de nivel superior que administren estos componentes de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="f93ae-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="f93ae-142">Media Foundation proporciona dos API de nivel superior para la codificación:</span><span class="sxs-lookup"><span data-stu-id="f93ae-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="f93ae-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sesión de medios](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="f93ae-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="f93ae-144">La sesión multimedia proporciona una canalización de un extremo a otro que mueve los datos desde el origen de medios, a través de los códecs y, por último, al receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="f93ae-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="f93ae-145">La aplicación controla la sesión multimedia y recibe los eventos de estado de la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="f93ae-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="f93ae-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lector de origen](source-reader.md) más [escritor de receptor](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="f93ae-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="f93ae-147">El lector de origen ajusta el origen de medios y, opcionalmente, los descodificadores.</span><span class="sxs-lookup"><span data-stu-id="f93ae-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="f93ae-148">Proporciona ejemplos codificados o descodificados en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f93ae-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="f93ae-149">El escritor del receptor incluye el receptor de medios y, opcionalmente, los codificadores.</span><span class="sxs-lookup"><span data-stu-id="f93ae-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="f93ae-150">La aplicación pasa ejemplos al escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="f93ae-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="f93ae-151">En el diagrama siguiente se muestra la sesión multimedia:</span><span class="sxs-lookup"><span data-stu-id="f93ae-151">The following diagram shows the Media Session:</span></span>

![diagrama que muestra cómo la sesión multimedia realiza la transcodificación](images/encoding01.png)

<span data-ttu-id="f93ae-153">La [API de Transcode](transcode-api.md) (el cuadro sombreado azul) es un conjunto de API incorporadas en Windows 7, que facilitan la configuración de la sesión multimedia para la codificación.</span><span class="sxs-lookup"><span data-stu-id="f93ae-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="f93ae-154">En el diagrama siguiente se muestra el lector de origen y el escritor del receptor:</span><span class="sxs-lookup"><span data-stu-id="f93ae-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![diagrama que muestra la transcodificación con el lector de origen y el escritor del receptor](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="f93ae-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f93ae-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f93ae-157">Codificación y creación de archivos</span><span class="sxs-lookup"><span data-stu-id="f93ae-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="f93ae-158">Programación de Media Foundation: conceptos básicos</span><span class="sxs-lookup"><span data-stu-id="f93ae-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



