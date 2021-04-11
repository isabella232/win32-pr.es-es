---
title: El asignador MIDI
description: El asignador MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimedia, asignador MIDI
- multimedia, asignador MIDI
- audio multimedia, asignador MIDI
- audio, asignador MIDI
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, acerca de
- Asignador MIDI, origen
- Asignador de MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075548"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="7780c-112">El asignador MIDI</span><span class="sxs-lookup"><span data-stu-id="7780c-112">The MIDI Mapper</span></span>

<span data-ttu-id="7780c-113">Los servicios de revisión estándar del asignador MIDI proporcionan la reproducción de archivos MIDI independientes del dispositivo para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7780c-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="7780c-114">El asignador MIDI se puede usar con el secuenciador MIDI de MCI o con los servicios de salida MIDI de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="7780c-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="7780c-115">A menos que se indique lo contrario, todas las referencias a números de canal MIDI usan los números de canal lógico del 1 al 16.</span><span class="sxs-lookup"><span data-stu-id="7780c-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="7780c-116">Estos números de canal lógico se corresponden con los números de canal físico del 0 al 15 que, en realidad, forman parte del mensaje MIDI.</span><span class="sxs-lookup"><span data-stu-id="7780c-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="7780c-117">Todas las referencias a los valores de clave y cambio de programa MIDI usan los valores físicos del 0 al 127.</span><span class="sxs-lookup"><span data-stu-id="7780c-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="7780c-118">Todos los números son decimales a menos que estén precedidos por el prefijo "0x", en cuyo caso son hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="7780c-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="7780c-119">En la explicación del Mapeador MIDI, el término *origen* hace referencia al lado de entrada del asignador MIDI.</span><span class="sxs-lookup"><span data-stu-id="7780c-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="7780c-120">El término *destino* hace referencia al lado de salida del asignador MIDI.</span><span class="sxs-lookup"><span data-stu-id="7780c-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="7780c-121">Por ejemplo, un canal de origen es el canal MIDI de un mensaje enviado al asignador de MIDI y un canal de destino es el canal MIDI de un mensaje enviado desde el asignador MIDI a un dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="7780c-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="7780c-122">El asignador de MIDI y Windows</span><span class="sxs-lookup"><span data-stu-id="7780c-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="7780c-123">Arquitectura del asignador MIDI</span><span class="sxs-lookup"><span data-stu-id="7780c-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="7780c-124">Asignación de canal</span><span class="sxs-lookup"><span data-stu-id="7780c-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="7780c-125">Mapas de revisiones</span><span class="sxs-lookup"><span data-stu-id="7780c-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="7780c-126">El volumen escalar</span><span class="sxs-lookup"><span data-stu-id="7780c-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="7780c-127">Mapas de claves</span><span class="sxs-lookup"><span data-stu-id="7780c-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="7780c-128">Resumen de mapas y mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="7780c-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




