---
title: Índices
description: Índices
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, índices
- Advanced Systems Format (ASF), índices
- ASF (formato de sistemas avanzados), índices
- SDK de Windows Media Format, índices temporales
- Advanced Systems Format (ASF), índices temporales
- ASF (formato de sistemas avanzados), índices temporales
- SDK de Windows Media Format, índices basados en marcos
- Advanced Systems Format (ASF), índices basados en tramas
- ASF (formato de sistemas avanzados), índices basados en tramas
- SDK de Windows Media Format, códigos de tiempo SMPTE
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- índices, acerca de
- índices temporales
- índices basados en marcos
- Códigos de tiempo SMPTE, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903750"
---
# <a name="indexes"></a><span data-ttu-id="3b451-119">Índices</span><span class="sxs-lookup"><span data-stu-id="3b451-119">Indexes</span></span>

<span data-ttu-id="3b451-120">Un requisito común para las aplicaciones que leen archivos multimedia digitales es la capacidad de buscar en un punto específico del contenido.</span><span class="sxs-lookup"><span data-stu-id="3b451-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="3b451-121">La búsqueda puede ser difícil porque no hay ninguna garantía de que los distintos flujos de un archivo tienen muestras con horas de inicio simultáneas.</span><span class="sxs-lookup"><span data-stu-id="3b451-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="3b451-122">Este problema se soluciona con el uso de *índices*.</span><span class="sxs-lookup"><span data-stu-id="3b451-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="3b451-123">Un índice es un objeto de un archivo ASF que equipara las muestras de vídeo con los tiempos de presentación.</span><span class="sxs-lookup"><span data-stu-id="3b451-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="3b451-124">No se requiere ningún índice para las secuencias de audio porque los datos de audio se conectan más estrechamente con el tiempo de presentación que los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b451-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="3b451-125">El objeto indexador del SDK de Windows Media Format puede crear tres tipos diferentes de índices: índices temporales, índices basados en marcos y índices de código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3b451-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="3b451-126">Los índices temporales son el tipo más común.</span><span class="sxs-lookup"><span data-stu-id="3b451-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="3b451-127">Simplemente son equivalentes a los ejemplos de vídeo con los tiempos de presentación correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3b451-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="3b451-128">Un índice basado en fotogramas equipara las muestras de vídeo con los números de fotogramas de vídeo y los tiempos de presentación.</span><span class="sxs-lookup"><span data-stu-id="3b451-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="3b451-129">Los números de fotogramas son especialmente útiles en aplicaciones que editan vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b451-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="3b451-130">Un índice de código de tiempo de SMTP es el tipo de índice más raro.</span><span class="sxs-lookup"><span data-stu-id="3b451-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="3b451-131">Utiliza el código de tiempo SMPTE como base del índice y solo se puede usar en flujos que tienen marcas de tiempo de SMPTE incluidas con sus ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3b451-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="3b451-132">Para obtener más información sobre el código de tiempo SMPTE, consulte [compatibilidad con código de tiempo SMPTE](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="3b451-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="3b451-133">Un archivo ASF puede contener un índice de cada tipo para cada flujo de vídeo que contenga.</span><span class="sxs-lookup"><span data-stu-id="3b451-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="3b451-134">De forma predeterminada, se incluye un índice temporal para cada secuencia de vídeo en los archivos creados por el objeto de escritura.</span><span class="sxs-lookup"><span data-stu-id="3b451-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="3b451-135">Puede cambiar la configuración de indexación automática de los archivos para que se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="3b451-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b451-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b451-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b451-137">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3b451-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="3b451-138">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="3b451-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="3b451-139">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="3b451-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="3b451-140">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="3b451-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




