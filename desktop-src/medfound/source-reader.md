---
description: El lector de origen es una alternativa al uso de la sesión multimedia y la canalización Microsoft Media Foundation para procesar los datos multimedia.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lector de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543798"
---
# <a name="source-reader"></a><span data-ttu-id="95257-103">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="95257-103">Source Reader</span></span>

<span data-ttu-id="95257-104">El lector de origen es una alternativa al uso de la [sesión multimedia](media-session.md) y la canalización Microsoft Media Foundation para procesar los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="95257-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="95257-105">¿Por qué usar el lector de origen?</span><span class="sxs-lookup"><span data-stu-id="95257-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="95257-106">Media Foundation proporciona una canalización optimizada para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="95257-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="95257-107">La canalización es de un extremo a otro, lo que significa que controla el flujo de datos desde el origen (como un archivo de vídeo) hasta el destino (por ejemplo, la presentación de gráficos).</span><span class="sxs-lookup"><span data-stu-id="95257-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="95257-108">Sin embargo, si desea leer o modificar los datos a medida que van a través de la canalización, debe escribir un complemento personalizado.</span><span class="sxs-lookup"><span data-stu-id="95257-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="95257-109">Esto requiere un conocimiento bastante profundo de la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="95257-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="95257-110">Para determinadas tareas, la creación de un nuevo complemento es demasiada sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="95257-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="95257-111">El lector de origen está diseñado para este tipo de situación, cuando desea obtener los datos sin procesar de un origen sin la sobrecarga de toda la canalización.</span><span class="sxs-lookup"><span data-stu-id="95257-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="95257-112">Internamente, el lector de origen contiene un puntero a un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="95257-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="95257-113">Un *origen multimedia* es un objeto Media Foundation que genera datos multimedia a partir de un origen externo, como un archivo multimedia o un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="95257-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="95257-114">El lector de origen administra todas las llamadas al método en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="95257-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="95257-115">(Para obtener más información acerca de los orígenes multimedia, consulte [orígenes multimedia](media-sources.md)).</span><span class="sxs-lookup"><span data-stu-id="95257-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="95257-116">Si el origen multimedia entrega datos comprimidos, puede utilizar el lector de origen para descodificar los datos.</span><span class="sxs-lookup"><span data-stu-id="95257-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="95257-117">En ese caso, el lector de código fuente cargará el descodificador correcto y administrará el flujo de datos entre el origen del medio y el descodificador.</span><span class="sxs-lookup"><span data-stu-id="95257-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="95257-118">El lector de origen también puede realizar un procesamiento de vídeo limitado: conversión de color de YUV a RGB-32 y desentrelazado de software, aunque estas operaciones no se recomiendan para la representación de vídeo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="95257-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="95257-119">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="95257-119">The following image illustrates this process.</span></span>

![diagrama del lector de origen](images/sourcereader.png)

<span data-ttu-id="95257-121">El lector de origen no envía los datos a un destino. depende de la aplicación usar los datos.</span><span class="sxs-lookup"><span data-stu-id="95257-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="95257-122">Por ejemplo, el lector de origen puede leer un archivo de vídeo, pero no representará el vídeo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="95257-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="95257-123">Además, el lector de origen no administra un reloj de presentación, controla los problemas de temporización ni sincroniza el vídeo con audio.</span><span class="sxs-lookup"><span data-stu-id="95257-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="95257-124">Considere la posibilidad de usar el lector de origen cuando:</span><span class="sxs-lookup"><span data-stu-id="95257-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="95257-125">Quiere obtener datos de un archivo multimedia sin preocuparse por la estructura de archivos subyacente.</span><span class="sxs-lookup"><span data-stu-id="95257-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="95257-126">Quiere obtener datos de un dispositivo de captura de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="95257-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="95257-127">Las tareas de procesamiento de datos no distinguen el tiempo o no se requiere un reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="95257-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="95257-128">Ya dispone de una canalización multimedia que no se basa en Media Foundation y desea incorporar los orígenes de Media Foundation multimedia a su propia canalización.</span><span class="sxs-lookup"><span data-stu-id="95257-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="95257-129">No se recomienda el lector de origen en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="95257-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="95257-130">Para contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="95257-130">For protected content.</span></span> <span data-ttu-id="95257-131">El lector de origen no admite la administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="95257-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="95257-132">Si le interesan los detalles de la estructura de archivos subyacente.</span><span class="sxs-lookup"><span data-stu-id="95257-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="95257-133">El lector de origen oculta ese tipo de detalle.</span><span class="sxs-lookup"><span data-stu-id="95257-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="95257-134">En esta sección</span><span class="sxs-lookup"><span data-stu-id="95257-134">In this section</span></span>



| <span data-ttu-id="95257-135">Tema</span><span class="sxs-lookup"><span data-stu-id="95257-135">Topic</span></span>                                                                                                        | <span data-ttu-id="95257-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="95257-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95257-137">Usar el lector de origen para procesar los datos multimedia</span><span class="sxs-lookup"><span data-stu-id="95257-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="95257-138">En este tema se describe cómo usar el lector de origen para procesar datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="95257-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="95257-139">Usar el lector de origen en modo asincrónico</span><span class="sxs-lookup"><span data-stu-id="95257-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="95257-140">En este tema se describe cómo usar el lector de origen en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="95257-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="95257-141">Tutorial: descodificar audio</span><span class="sxs-lookup"><span data-stu-id="95257-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="95257-142">En este tutorial se muestra cómo usar el lector de origen para descodificar el audio de un archivo multimedia y escribir el audio en un archivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="95257-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="95257-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95257-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95257-144">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95257-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="95257-145">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95257-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="95257-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="95257-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




