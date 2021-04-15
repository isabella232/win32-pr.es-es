---
description: En este tema se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea Guía de programación de Media Foundation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Información general de la arquitectura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104555620"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="f9640-104">Información general de la arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9640-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="f9640-105">En este tema se describe el diseño general de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f9640-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="f9640-106">Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea [Guía de programación de Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="f9640-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="f9640-107">En el diagrama siguiente se muestra una vista de alto nivel de la arquitectura de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f9640-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![diagrama que muestra una vista de alto nivel de la arquitectura de Media Foundation.](images/mfarch01.png)

<span data-ttu-id="f9640-109">Media Foundation proporciona dos modelos de programación distintos.</span><span class="sxs-lookup"><span data-stu-id="f9640-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="f9640-110">El primer modelo, que se muestra en el lado izquierdo del diagrama, utiliza una canalización de un extremo a otro para los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9640-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="f9640-111">La aplicación inicializa la canalización (por ejemplo, proporcionando la dirección URL de un archivo que se va a reproducir) y, a continuación, llama a los métodos para controlar el streaming.</span><span class="sxs-lookup"><span data-stu-id="f9640-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="f9640-112">En el segundo modelo, que se muestra en el lado derecho del diagrama, la aplicación extrae datos de un origen o los empuja a un destino (o ambos).</span><span class="sxs-lookup"><span data-stu-id="f9640-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="f9640-113">Este modelo es especialmente útil si necesita procesar los datos, porque la aplicación tiene acceso directo al flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="f9640-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="f9640-114">Primitivas y plataforma</span><span class="sxs-lookup"><span data-stu-id="f9640-114">Primitives and Platform</span></span>

<span data-ttu-id="f9640-115">A partir de la parte inferior del diagrama, los *primitivos* son objetos auxiliares que se utilizan en la API de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="f9640-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="f9640-116">[Los atributos](attributes-and-properties.md) son una manera genérica de almacenar información dentro de un objeto, como una lista de pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="f9640-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="f9640-117">Los [tipos de medios](media-types.md) describen el formato de un flujo de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9640-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="f9640-118">Los [búferes multimedia](media-buffers.md) contienen fragmentos de datos multimedia, como fotogramas de vídeo y muestras de audio, y se usan para transportar datos entre objetos.</span><span class="sxs-lookup"><span data-stu-id="f9640-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="f9640-119">Los [ejemplos de medios](media-samples.md) son contenedores de búferes multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9640-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="f9640-120">También contienen metadatos acerca de los búferes, como las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f9640-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="f9640-121">Las [API de Media Foundation Platform](media-foundation-platform-apis.md) proporcionan alguna funcionalidad básica que usa la canalización de Media Foundation, como las devoluciones de llamada asincrónicas y las colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="f9640-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="f9640-122">Es posible que algunas aplicaciones necesiten llamar a estas API directamente; Además, los necesitará si implementa un origen, una transformación o un receptor personalizado para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f9640-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="f9640-123">Canalización multimedia</span><span class="sxs-lookup"><span data-stu-id="f9640-123">Media Pipeline</span></span>

<span data-ttu-id="f9640-124">La canalización multimedia contiene tres tipos de objetos que generan o procesan datos multimedia:</span><span class="sxs-lookup"><span data-stu-id="f9640-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="f9640-125">Los [orígenes de medios](media-sources.md) introducen los datos en la canalización.</span><span class="sxs-lookup"><span data-stu-id="f9640-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="f9640-126">Un origen multimedia puede obtener datos de un archivo local, como un archivo de vídeo. desde un flujo de red; o desde un dispositivo de captura de hardware.</span><span class="sxs-lookup"><span data-stu-id="f9640-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="f9640-127">[Media Foundation transformaciones](media-foundation-transforms.md) (MFTs) procesan datos de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f9640-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="f9640-128">Los codificadores y descodificadores se implementan como MFTs.</span><span class="sxs-lookup"><span data-stu-id="f9640-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="f9640-129">Los [receptores de medios](media-sinks.md) consumen los datos; por ejemplo, mostrando vídeo en la pantalla, reproduciendo audio o escribiendo los datos en un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9640-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="f9640-130">Los terceros pueden implementar sus propios orígenes personalizados, receptores y MFTs; por ejemplo, para admitir nuevos formatos de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9640-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="f9640-131">La [sesión multimedia](media-session.md) controla el flujo de datos a través de la canalización y controla tareas como el control de calidad, la sincronización de audio y vídeo y la respuesta a los cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="f9640-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="f9640-132">Lector de origen y escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="f9640-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="f9640-133">El [lector de origen](source-reader.md) y el [escritor de receptores](sink-writer.md) proporcionan una manera alternativa de usar los componentes de Media Foundation básicos (orígenes de medios, transformaciones y receptores multimedia).</span><span class="sxs-lookup"><span data-stu-id="f9640-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="f9640-134">El lector de origen hospeda un origen de medios y cero o más descodificadores, mientras que el escritor de receptor hospeda un receptor de medios y cero o más codificadores.</span><span class="sxs-lookup"><span data-stu-id="f9640-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="f9640-135">Puede usar el lector de origen para obtener datos comprimidos o sin comprimir de un origen multimedia y usar el escritor de receptores para codificar datos y enviarlos a un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="f9640-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="f9640-136">El lector de origen y el escritor del receptor están disponibles en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9640-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="f9640-137">Este modelo de programación proporciona a la aplicación más control sobre el flujo de datos y también proporciona a la aplicación acceso directo a los datos desde el origen.</span><span class="sxs-lookup"><span data-stu-id="f9640-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9640-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9640-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9640-139">Media Foundation: conceptos esenciales</span><span class="sxs-lookup"><span data-stu-id="f9640-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="f9640-140">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9640-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



