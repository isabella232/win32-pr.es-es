---
title: Instrucciones de creación para archivos MIDI
description: Instrucciones de creación para archivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), instrucciones para la creación de archivos
- MIDI (interfaz digital de instrumentos musicales), instrucciones para la creación de archivos
- creación de archivos MIDI, instrucciones para la creación de archivos
- asignaciones estándar de revisión MIDI
- asignaciones de claves MIDI estándar
- Interfaz digital de instrumentos musicales (MIDI), asignaciones de revisiones estándar
- MIDI (interfaz digital de instrumentos musicales), asignaciones de revisiones estándar
- Interfaz digital de instrumentos musicales (MIDI), asignaciones de claves estándar
- MIDI (interfaz digital de instrumentos musicales), asignaciones de clave estándar
- creación de archivos MIDI, asignaciones de revisiones estándar
- crear archivos MIDI, asignaciones de clave estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076279"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="aa179-114">Instrucciones de creación para archivos MIDI</span><span class="sxs-lookup"><span data-stu-id="aa179-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="aa179-115">Siga estas instrucciones para crear archivos MIDI independientes del dispositivo para Windows:</span><span class="sxs-lookup"><span data-stu-id="aa179-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="aa179-116">Use las [asignaciones estándar de revisión de MIDI](standard-midi-patch-assignments.md) y las [asignaciones de clave MIDI estándar](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="aa179-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="aa179-117">Envíe siempre un mensaje de cambio de programa a un canal para seleccionar una revisión antes de enviar otros mensajes a ese canal.</span><span class="sxs-lookup"><span data-stu-id="aa179-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="aa179-118">Para los dos canales de percusión (10 y 16), seleccione el número de programa 0.</span><span class="sxs-lookup"><span data-stu-id="aa179-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="aa179-119">Siga siempre un mensaje de cambio de programa MIDI con un mensaje de controlador de volumen principal MIDI (número de controlador 7) para establecer el volumen relativo de la revisión.</span><span class="sxs-lookup"><span data-stu-id="aa179-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="aa179-120">Use un valor de 80 (0x50) para el controlador de volumen principal para los niveles de escucha normales.</span><span class="sxs-lookup"><span data-stu-id="aa179-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="aa179-121">Para niveles más silenciosos o más altos, puede usar valores inferiores o superiores.</span><span class="sxs-lookup"><span data-stu-id="aa179-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="aa179-122">Use solo los siguientes mensajes MIDI: tenga en cuenta la velocidad, el cambio de la nota, la desactivación, el cambio de programa, el plegado de paso, el volumen principal (controlador 7) y el pedal del amortiguador (controlador 64).</span><span class="sxs-lookup"><span data-stu-id="aa179-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="aa179-123">Los sintetizadores internos son necesarios para responder a estos mensajes y la mayoría de los instrumentos musicales MIDI también responden a ellos.</span><span class="sxs-lookup"><span data-stu-id="aa179-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 




