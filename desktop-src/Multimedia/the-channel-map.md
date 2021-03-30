---
title: Asignación de canal
description: Asignación de canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapa de canales
- mapa de canal
- Asignador de MIDI, mensajes de canal
- Mensajes del canal MIDI
- mensajes de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148828"
---
# <a name="the-channel-map"></a><span data-ttu-id="11a50-110">Asignación de canal</span><span class="sxs-lookup"><span data-stu-id="11a50-110">The Channel Map</span></span>

<span data-ttu-id="11a50-111">La asignación de canal afecta a todos los mensajes del canal MIDI.</span><span class="sxs-lookup"><span data-stu-id="11a50-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="11a50-112">Los mensajes del canal MIDI incluyen los mensajes de Nota: on, note-off, polyphonic-Key-aftertouch, control-Change, Program-Change, Channel-aftertouch y Pitch-Bend-Change.</span><span class="sxs-lookup"><span data-stu-id="11a50-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="11a50-113">El asignador de MIDI utiliza un mapa de canal único con una entrada para cada uno de los 16 canales MIDI.</span><span class="sxs-lookup"><span data-stu-id="11a50-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="11a50-114">Cada entrada de asignación de canal especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="11a50-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="11a50-115">Un canal de destino para el mensaje MIDI</span><span class="sxs-lookup"><span data-stu-id="11a50-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="11a50-116">Un dispositivo de salida de destino para el mensaje MIDI</span><span class="sxs-lookup"><span data-stu-id="11a50-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="11a50-117">Una asignación de revisión opcional que especifica otras modificaciones posibles para el mensaje MIDI</span><span class="sxs-lookup"><span data-stu-id="11a50-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="11a50-118">El canal de destino se establece en uno de los 16 canales MIDI.</span><span class="sxs-lookup"><span data-stu-id="11a50-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="11a50-119">Los mensajes MIDI se modifican para reflejar cada nueva asignación de canal.</span><span class="sxs-lookup"><span data-stu-id="11a50-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="11a50-120">Por ejemplo, si la entrada de canal de destino para el canal de MIDI 4 está establecida en 6, todos los mensajes MIDI enviados al canal 4 se asignarán al canal 6, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="11a50-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![imagen MIDI asignada](images/mmap-a05.gif)

<span data-ttu-id="11a50-122">En este ejemplo, el byte de estado de MIDI 0x93 se asigna a 0x95.</span><span class="sxs-lookup"><span data-stu-id="11a50-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="11a50-123">El orden inferior de un byte de estado de MIDI especifica el número de canal.</span><span class="sxs-lookup"><span data-stu-id="11a50-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="11a50-124">Los canales de origen se establecen en activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="11a50-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="11a50-125">Los mensajes enviados a los canales de origen inactivos se omiten, por lo que un canal inactivo está en vigor o desactivado.</span><span class="sxs-lookup"><span data-stu-id="11a50-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="11a50-126">El dispositivo de salida de destino se establece en uno de los dispositivos de salida MIDI disponibles.</span><span class="sxs-lookup"><span data-stu-id="11a50-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="11a50-127">Un dispositivo de salida MIDI puede ser un sintetizador interno o un puerto de salida MIDI físico.</span><span class="sxs-lookup"><span data-stu-id="11a50-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="11a50-128">Los mensajes del sistema MIDI son mensajes MIDI (con el estado bytes) de 0xF0 a 0xFF.</span><span class="sxs-lookup"><span data-stu-id="11a50-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="11a50-129">No hay ningún canal asociado a los mensajes del sistema MIDI, por lo que no se pueden asignar.</span><span class="sxs-lookup"><span data-stu-id="11a50-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="11a50-130">Los mensajes del sistema MIDI se envían a todos los dispositivos de salida MIDI que aparecen en una asignación de canal.</span><span class="sxs-lookup"><span data-stu-id="11a50-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




