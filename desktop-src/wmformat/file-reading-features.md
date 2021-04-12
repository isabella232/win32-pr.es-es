---
title: Características de lectura de archivos
description: Características de lectura de archivos
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- SDK de Windows Media Format, características de lectura de archivos
- SDK de Windows Media Format, lectura asincrónica de archivos
- SDK de Windows Media Format, lectura sincrónica de archivos
- Advanced Systems Format (ASF), características de lectura de archivos
- ASF (formato de sistemas avanzados), características de lectura de archivos
- Advanced Systems Format (ASF), lectura asincrónica de archivos
- ASF (formato de sistemas avanzados), lectura asincrónica de archivos
- Advanced Systems Format (ASF), lectura de archivos sincrónicos
- ASF (formato de sistemas avanzados), lectura de archivos sincrónicos
- lectura asincrónica de archivos
- lectura de archivos sincrónicos
- lectores sincrónicos, características de lectura de archivos
- lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357683"
---
# <a name="file-reading-features"></a><span data-ttu-id="28385-116">Características de lectura de archivos</span><span class="sxs-lookup"><span data-stu-id="28385-116">File Reading Features</span></span>

<span data-ttu-id="28385-117">La lectura de archivos ASF es una de las características principales del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="28385-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="28385-118">Se admiten dos tipos de lectura: asincrónicos y sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="28385-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="28385-119">El objeto lector controla la lectura asincrónica de archivos.</span><span class="sxs-lookup"><span data-stu-id="28385-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="28385-120">El objeto lector sincrónico se usa para leer archivos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="28385-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="28385-121">Para obtener más información sobre los diferentes objetos de lectura, vea [objeto lector](reader-object.md) y [objeto lector sincrónico](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="28385-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="28385-122">En el escenario de lectura de archivos asincrónico más básico, debe implementar un método de devolución de llamada al que el objeto lector llamará cuando los ejemplos estén listos.</span><span class="sxs-lookup"><span data-stu-id="28385-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="28385-123">Después de empezar a leer un archivo, la aplicación espera a que se entreguen los ejemplos en el método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="28385-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="28385-124">La lectura asincrónica es útil para las aplicaciones de reproductor y admite características no disponibles con lectura sincrónica.</span><span class="sxs-lookup"><span data-stu-id="28385-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="28385-125">Si la aplicación necesita leer archivos de una ubicación de red o interactuar con un servidor que ejecuta Windows Media Services, debe usar el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="28385-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="28385-126">El inconveniente del objeto lector es que se usa un subproceso independiente para cada salida entregada.</span><span class="sxs-lookup"><span data-stu-id="28385-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="28385-127">Además, el objeto de lector no es tan flexible como el lector sincrónico en cómo puede proporcionar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="28385-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="28385-128">Con el lector sincrónico no es necesario usar ningún método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="28385-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="28385-129">En su lugar, se selecciona una parte del archivo que se va a leer y se recuperan los ejemplos de uno en uno con llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="28385-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="28385-130">El lector sincrónico está bien adaptado a las necesidades de las aplicaciones de edición de contenido, donde es esencial el acceso rápido a ejemplos específicos.</span><span class="sxs-lookup"><span data-stu-id="28385-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="28385-131">Dado que el lector sincrónico no usa ningún método de devolución de llamada, puede crear aplicaciones para leer archivos ASF con una sobrecarga de codificación mínima.</span><span class="sxs-lookup"><span data-stu-id="28385-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="28385-132">Sin embargo, el lector sincrónico no puede abrir un archivo desde una ubicación de red o interactuar con un servidor que ejecuta Windows Media Services o leer archivos protegidos con [*DRM*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="28385-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="28385-133">En los temas siguientes se describen las características del lector y el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="28385-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="28385-134">Tema</span><span class="sxs-lookup"><span data-stu-id="28385-134">Topic</span></span>                                                              | <span data-ttu-id="28385-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="28385-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28385-136">Compatibilidad de ejemplo asignada por el usuario</span><span class="sxs-lookup"><span data-stu-id="28385-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="28385-137">Describe la asignación de búferes en el lector y el lector sincrónico, y cómo la asignación de usuarios puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="28385-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="28385-138">Enumeración del formato de salida</span><span class="sxs-lookup"><span data-stu-id="28385-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="28385-139">Describe la enumeración del formato de salida.</span><span class="sxs-lookup"><span data-stu-id="28385-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="28385-140">Además, los siguientes temas de la sección características de escritura también se aplican a la lectura de archivos:</span><span class="sxs-lookup"><span data-stu-id="28385-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="28385-141">Cambio de tamaño de vídeo</span><span class="sxs-lookup"><span data-stu-id="28385-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="28385-142">Conversión de espacio de colores</span><span class="sxs-lookup"><span data-stu-id="28385-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="28385-143">Remuestreo de audio</span><span class="sxs-lookup"><span data-stu-id="28385-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="28385-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28385-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28385-145">**Características**</span><span class="sxs-lookup"><span data-stu-id="28385-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="28385-146">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="28385-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




