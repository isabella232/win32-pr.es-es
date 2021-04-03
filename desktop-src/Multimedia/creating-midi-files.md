---
title: Crear archivos MIDI
description: Crear archivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimedia, crear archivos MIDI
- multimedia, crear archivos MIDI
- audio multimedia, crear archivos MIDI
- audio, creación de archivos MIDI
- Interfaz digital de instrumentos musicales (MIDI), crear archivos
- MIDI (interfaz digital de instrumentos musicales), crear archivos
- crear archivos MIDI, acerca de
- Asociación de fabricantes de MIDI (MMA)
- MMA (Asociación de fabricantes de MIDI)
- Especificación detallada de MIDI
- Especificación de archivos MIDI estándar
- Especificación MIDI general (GM)
- Especificación GM (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075442"
---
# <a name="creating-midi-files"></a><span data-ttu-id="f21a4-116">Crear archivos MIDI</span><span class="sxs-lookup"><span data-stu-id="f21a4-116">Creating MIDI Files</span></span>

<span data-ttu-id="f21a4-117">Las especificaciones de la interfaz digital de instrumentos musicales (MIDI) están publicadas por y son material protegido por derechos de autor de la Asociación de fabricantes de MIDI (MMA).</span><span class="sxs-lookup"><span data-stu-id="f21a4-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="f21a4-118">En la lista siguiente se describen las especificaciones de mayor interés general:</span><span class="sxs-lookup"><span data-stu-id="f21a4-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="f21a4-119">Especificación detallada de MIDI</span><span class="sxs-lookup"><span data-stu-id="f21a4-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="f21a4-120">La especificación detallada de MIDI explica los protocolos de hardware y software de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f21a4-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="f21a4-121">Esto resulta útil para aquellos que desarrollan aplicaciones multimedia que implementan la compatibilidad con MIDI mediante el uso de funciones MIDI para grabar, editar o reproducir datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="f21a4-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="f21a4-122">Archivos MIDI estándar 1,0</span><span class="sxs-lookup"><span data-stu-id="f21a4-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="f21a4-123">La especificación de archivos MIDI estándar define una manera de intercambiar datos MIDI con marca de tiempo entre diferentes aplicaciones en la misma plataforma de hardware o en distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="f21a4-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="f21a4-124">Esto resulta útil para los programadores que escriben aplicaciones que leen y analizan archivos de disco que contienen datos MIDI o escriben archivos de datos MIDI en el disco.</span><span class="sxs-lookup"><span data-stu-id="f21a4-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="f21a4-125">Nivel de sistema MIDI general 1</span><span class="sxs-lookup"><span data-stu-id="f21a4-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="f21a4-126">La especificación MIDI general (GM) define una configuración de MIDI mínima de un "sistema MIDI general".</span><span class="sxs-lookup"><span data-stu-id="f21a4-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="f21a4-127">Este sistema se compone de una clase específica de dispositivos de reproducción MIDI y es de interés para los desarrolladores multimedia que crean archivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="f21a4-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="f21a4-128">La mayoría de las tarjetas de sonido de PC y los sintetizadores MIDI fabricados hoy en día son compatibles con la especificación GM.</span><span class="sxs-lookup"><span data-stu-id="f21a4-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="f21a4-129">Por lo general, los archivos MIDI que se crean con la especificación GM deben sonar tal y como están destinados a sonar, independientemente del dispositivo compatible con GM en el que se reproduzcan.</span><span class="sxs-lookup"><span data-stu-id="f21a4-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="f21a4-130">Para permitir que los archivos MIDI tengan un formato viable para representar música en la informática multimedia, Windows sigue la especificación general de nivel 1 del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="f21a4-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="f21a4-131">En los temas siguientes se proporcionan instrucciones adicionales para la creación de MIDI:</span><span class="sxs-lookup"><span data-stu-id="f21a4-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="f21a4-132">Instrucciones de creación para archivos MIDI</span><span class="sxs-lookup"><span data-stu-id="f21a4-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="f21a4-133">Asignaciones estándar de revisión MIDI</span><span class="sxs-lookup"><span data-stu-id="f21a4-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="f21a4-134">Asignaciones de claves MIDI estándar</span><span class="sxs-lookup"><span data-stu-id="f21a4-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 




