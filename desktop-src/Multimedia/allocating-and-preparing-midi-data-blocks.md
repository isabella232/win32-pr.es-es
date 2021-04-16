---
title: Asignación y preparación de bloques de datos MIDI
description: Asignación y preparación de bloques de datos MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignar bloques de datos
- MIDI (interfaz digital de instrumentos musicales), asignar bloques de datos
- Servicios MIDI, asignar bloques de datos
- asignación de bloques de datos MIDI
- Interfaz digital de instrumentos musicales (MIDI), preparar bloques de datos
- MIDI (interfaz digital de instrumentos musicales), preparar bloques de datos
- Servicios MIDI, preparar bloques de datos
- preparación de bloques de datos MIDI
- Interfaz digital de instrumentos musicales (MIDI), bloques de datos
- MIDI (interfaz digital de instrumentos musicales), bloques de datos
- Servicios MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676375"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="f813d-114">Asignación y preparación de bloques de datos MIDI</span><span class="sxs-lookup"><span data-stu-id="f813d-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="f813d-115">Las funciones [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)y [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requieren que las aplicaciones asignen bloques de datos para pasarlos a los controladores de dispositivos con fines de reproducción o grabación.</span><span class="sxs-lookup"><span data-stu-id="f813d-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="f813d-116">Cada una de estas funciones usa una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para describir su bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="f813d-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="f813d-117">Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el búfer y la estructura de encabezado que describe el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="f813d-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="f813d-118">Windows proporciona las siguientes funciones para preparar y limpiar los bloques de datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="f813d-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="f813d-119">Value</span><span class="sxs-lookup"><span data-stu-id="f813d-119">Value</span></span>                                                    | <span data-ttu-id="f813d-120">Significado</span><span class="sxs-lookup"><span data-stu-id="f813d-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f813d-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f813d-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="f813d-122">Prepara un bloque de datos de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f813d-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="f813d-123">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f813d-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="f813d-124">Limpia la preparación de un bloque de datos de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f813d-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="f813d-125">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f813d-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="f813d-126">Prepara un bloque de datos de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="f813d-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="f813d-127">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f813d-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="f813d-128">Limpia la preparación de un bloque de datos de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="f813d-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="f813d-129">Antes de pasar un bloque de datos MIDI a un controlador de dispositivo, debe preparar el búfer pasándolo a la función [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) .</span><span class="sxs-lookup"><span data-stu-id="f813d-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="f813d-130">Cuando el controlador de dispositivo finaliza con el búfer y lo devuelve, debe limpiar esta preparación pasando el búfer a la función [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="f813d-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f813d-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f813d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f813d-132">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="f813d-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 