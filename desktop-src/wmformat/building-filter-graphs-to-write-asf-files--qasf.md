---
title: Generar gráficos de filtro para escribir archivos ASF (QASF)
description: Generar gráficos de filtro para escribir archivos ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- SDK de Windows Media Format, crear gráficos de filtros (QASF)
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, escribir archivos ASF (QASF)
- Advanced Systems Format (ASF), crear gráficos de filtros (QASF)
- ASF (formato de sistemas avanzados), crear gráficos de filtros (QASF)
- Advanced Systems Format (ASF), escritura (QASF)
- ASF (formato de sistemas avanzados), escritura (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, crear gráficos de filtros (QASF)
- DirectShow, escribir archivos ASF (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714121"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="8d02a-118">Generar gráficos de filtro para escribir archivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="8d02a-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="8d02a-119">Las aplicaciones basadas en DirectShow normalmente usan uno de los tres tipos básicos de gráficos de filtros al crear contenido basado en Windows Media:</span><span class="sxs-lookup"><span data-stu-id="8d02a-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="8d02a-120">Filtre los gráficos para convertir o transcodificar contenido de otro formato en formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8d02a-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="8d02a-121">Filtre los gráficos para insertar contenido que no esté basado en Windows Media (formatos de secuencia nativo) en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="8d02a-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="8d02a-122">Filtre los gráficos para capturar datos activos y codificarlos inmediatamente en el formato de Windows Media antes de guardarlos en el disco.</span><span class="sxs-lookup"><span data-stu-id="8d02a-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="8d02a-123">Cada tipo de gráfico de filtro se describe con más detalle en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="8d02a-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="8d02a-124">Sección</span><span class="sxs-lookup"><span data-stu-id="8d02a-124">Section</span></span>                                                                                                             | <span data-ttu-id="8d02a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d02a-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d02a-126">Transcodificar archivos (QASF)</span><span class="sxs-lookup"><span data-stu-id="8d02a-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="8d02a-127">Describe cómo crear gráficos de filtros de transcodificación de archivos.</span><span class="sxs-lookup"><span data-stu-id="8d02a-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="8d02a-128">Insertar formatos de secuencias nativas en archivos ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="8d02a-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="8d02a-129">Describe cómo colocar cualquier tipo de datos de audio o vídeo comprimidos o no comprimidos en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="8d02a-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="8d02a-130">Captura directa desde un dispositivo a un archivo ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="8d02a-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="8d02a-131">Describe cómo crear gráficos de filtros de captura que se generan en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="8d02a-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




