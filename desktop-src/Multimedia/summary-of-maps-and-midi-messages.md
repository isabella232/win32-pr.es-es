---
title: Resumen de mapas y mensajes MIDI
description: Resumen de mapas y mensajes MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapa de canales
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas de claves
- mapa de canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778840"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="5feb1-111">Resumen de mapas y mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="5feb1-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="5feb1-112">A continuación se indican los bytes de estado de los mensajes MIDI y los tipos de mapa que afectan a cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="5feb1-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="5feb1-113">Estado de MIDI</span><span class="sxs-lookup"><span data-stu-id="5feb1-113">MIDI status</span></span> | <span data-ttu-id="5feb1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5feb1-114">Description</span></span>               | <span data-ttu-id="5feb1-115">Tipos de asignación</span><span class="sxs-lookup"><span data-stu-id="5feb1-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="5feb1-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="5feb1-116">0x80-0x8F</span></span>   | <span data-ttu-id="5feb1-117">Nota OFF</span><span class="sxs-lookup"><span data-stu-id="5feb1-117">Note off</span></span>                  | <span data-ttu-id="5feb1-118">Mapas de canales, mapas de claves</span><span class="sxs-lookup"><span data-stu-id="5feb1-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="5feb1-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="5feb1-119">0x90-0x9F</span></span>   | <span data-ttu-id="5feb1-120">Nota sobre </span><span class="sxs-lookup"><span data-stu-id="5feb1-120">Note on</span></span>                   | <span data-ttu-id="5feb1-121">Mapas de canales, mapas de claves</span><span class="sxs-lookup"><span data-stu-id="5feb1-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="5feb1-122">0xA0-0xAF</span><span class="sxs-lookup"><span data-stu-id="5feb1-122">0xA0-0xAF</span></span>   | <span data-ttu-id="5feb1-123">Polyphonic-clave aftertouch</span><span class="sxs-lookup"><span data-stu-id="5feb1-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="5feb1-124">Mapas de canales, mapas de claves</span><span class="sxs-lookup"><span data-stu-id="5feb1-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="5feb1-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="5feb1-125">0xB0-0xBF</span></span>   | <span data-ttu-id="5feb1-126">Cambio de control</span><span class="sxs-lookup"><span data-stu-id="5feb1-126">Control change</span></span>            | <span data-ttu-id="5feb1-127">Mapas de canales, mapas de revisiones</span><span class="sxs-lookup"><span data-stu-id="5feb1-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="5feb1-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="5feb1-128">0xC0-0xCF</span></span>   | <span data-ttu-id="5feb1-129">Cambio de programa</span><span class="sxs-lookup"><span data-stu-id="5feb1-129">Program change</span></span>            | <span data-ttu-id="5feb1-130">Mapas de canales, mapas de revisiones</span><span class="sxs-lookup"><span data-stu-id="5feb1-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="5feb1-131">0xD0-0xDF</span><span class="sxs-lookup"><span data-stu-id="5feb1-131">0xD0-0xDF</span></span>   | <span data-ttu-id="5feb1-132">Canal aftertouch</span><span class="sxs-lookup"><span data-stu-id="5feb1-132">Channel aftertouch</span></span>        | <span data-ttu-id="5feb1-133">Mapas de canal</span><span class="sxs-lookup"><span data-stu-id="5feb1-133">Channel maps</span></span>             |
| <span data-ttu-id="5feb1-134">0xE0-0xEF</span><span class="sxs-lookup"><span data-stu-id="5feb1-134">0xE0-0xEF</span></span>   | <span data-ttu-id="5feb1-135">Cambio de plegado de tono</span><span class="sxs-lookup"><span data-stu-id="5feb1-135">Pitch-bend change</span></span>         | <span data-ttu-id="5feb1-136">Mapas de canal</span><span class="sxs-lookup"><span data-stu-id="5feb1-136">Channel maps</span></span>             |
| <span data-ttu-id="5feb1-137">0xF0-0xFF</span><span class="sxs-lookup"><span data-stu-id="5feb1-137">0xF0-0xFF</span></span>   | <span data-ttu-id="5feb1-138">System</span><span class="sxs-lookup"><span data-stu-id="5feb1-138">System</span></span>                    | <span data-ttu-id="5feb1-139">No asignado</span><span class="sxs-lookup"><span data-stu-id="5feb1-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="5feb1-140">Los cuatro bits de orden superior representan el valor de estado.</span><span class="sxs-lookup"><span data-stu-id="5feb1-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="5feb1-141">Los cuatro bits de orden inferior representan la información del canal.</span><span class="sxs-lookup"><span data-stu-id="5feb1-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="5feb1-142">Las asignaciones de revisión solo afectan al controlador 7 (volumen principal).</span><span class="sxs-lookup"><span data-stu-id="5feb1-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="5feb1-143">Los mensajes del sistema se envían a todos los dispositivos que aparecen en una asignación de canal.</span><span class="sxs-lookup"><span data-stu-id="5feb1-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




