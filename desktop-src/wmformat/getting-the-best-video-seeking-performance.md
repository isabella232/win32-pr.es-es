---
title: Obtención del mejor rendimiento de búsqueda de vídeo
description: Obtención del mejor rendimiento de búsqueda de vídeo
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, mejor rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), mejor rendimiento de búsqueda de vídeo
- ASF (formato de sistemas avanzados), mejor rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), vídeo que busca rendimiento
- ASF (formato de sistemas avanzados), rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), performance
- ASF (formato de sistemas avanzados), rendimiento
- búsqueda en vídeo
- rendimiento, búsqueda de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695382"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="e27dc-112">Obtención del mejor rendimiento de búsqueda de vídeo</span><span class="sxs-lookup"><span data-stu-id="e27dc-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="e27dc-113">La búsqueda de contenido en un archivo es una operación muy común que puede suponer un problema de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e27dc-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="e27dc-114">El vídeo codificado con el códec de Windows Media Video 9 se compone principalmente de fotogramas Delta, que solo registran los cambios en relación con el fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="e27dc-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="e27dc-115">Reconstruir fotogramas Delta lleva tiempo, especialmente si los fotogramas clave están alejados.</span><span class="sxs-lookup"><span data-stu-id="e27dc-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="e27dc-116">Para obtener más información sobre cómo configurar fotogramas clave para una búsqueda eficaz, consulte [configuración de secuencias de vídeo para buscar el rendimiento](configuring-video-streams-for-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="e27dc-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="e27dc-117">Además de la configuración adecuada, puede mejorar el rendimiento de búsqueda mediante la indexación de fotogramas para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e27dc-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="e27dc-118">La búsqueda de un número de marco suele ser más rápida que la búsqueda en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="e27dc-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="e27dc-119">Si busca en un archivo con varias secuencias, debe seleccionar solo los flujos que sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="e27dc-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="e27dc-120">Cada flujo configurado para lectura afectará al rendimiento de la búsqueda, ya que todas las secuencias seleccionadas se sincronizan cuando se busca un punto en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e27dc-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e27dc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e27dc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e27dc-122">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e27dc-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="e27dc-123">**Para buscar por número de marco mediante el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="e27dc-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e27dc-124">**Para buscar por número de marco mediante el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="e27dc-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e27dc-125">**Para buscar por tiempo mediante el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="e27dc-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e27dc-126">**Para buscar por tiempo mediante el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="e27dc-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




