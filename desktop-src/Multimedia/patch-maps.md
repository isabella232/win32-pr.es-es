---
title: Mapas de revisiones
description: Mapas de revisiones
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapas de revisiones
- mapas de revisiones
- 'Programa MIDI: mensajes de cambio'
- Mensajes de controlador de volumen MIDI
- mensajes de cambio de programa
- mensajes de controlador de volumen
- Asignador de MIDI, mensajes de cambio de programa
- Asignador de MIDI, mensajes de controlador de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357008"
---
# <a name="patch-maps"></a><span data-ttu-id="e4fc9-113">Mapas de revisiones</span><span class="sxs-lookup"><span data-stu-id="e4fc9-113">Patch Maps</span></span>

<span data-ttu-id="e4fc9-114">Cada entrada de mapa de canal puede tener una asignación de revisión asociada.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="e4fc9-115">Las asignaciones de revisiones afectan a los mensajes de cambio de programa MIDI y de controlador de volumen.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="e4fc9-116">Los mensajes de cambio de programa indican a un sintetizador que cambie el sonido del instrumento (revisión) de un canal especificado.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="e4fc9-117">Los mensajes de Volume Controller establecen el volumen de un canal.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="e4fc9-118">Una asignación de revisión tiene una tabla de traducción con una entrada para cada uno de los valores de cambio de programa de 128.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="e4fc9-119">Cada asignación de revisión especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4fc9-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="e4fc9-120">Valor de cambio de programa de destino.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-120">A destination program-change value.</span></span>
-   <span data-ttu-id="e4fc9-121">Escalar del volumen.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-121">A volume scalar.</span></span> <span data-ttu-id="e4fc9-122">(Para obtener más información, vea [el volumen escalar](the-volume-scalar.md)).</span><span class="sxs-lookup"><span data-stu-id="e4fc9-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="e4fc9-123">Un mapa de claves opcional.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-123">An optional key map.</span></span> <span data-ttu-id="e4fc9-124">(Para obtener más información, consulte [mapas de claves](key-maps.md)).</span><span class="sxs-lookup"><span data-stu-id="e4fc9-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="e4fc9-125">Cuando el asignador MIDI recibe los mensajes de cambio de programa, el valor de cambio de programa de destino se sustituye por el valor de cambio de programa en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="e4fc9-126">Por ejemplo, si el programa de destino-Change Value for Program-Change 16 es 18, el asignador MIDI modifica el mensaje de cambio de programa MIDI tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![imagen del asignador MIDI](images/mmap-a03.gif)

 

 




