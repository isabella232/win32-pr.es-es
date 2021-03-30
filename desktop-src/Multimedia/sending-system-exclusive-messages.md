---
title: Envío de mensajes de System-Exclusive
description: Envío de mensajes de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), mensajes exclusivos del sistema
- MIDI (interfaz digital de instrumentos musicales), mensajes exclusivos del sistema
- reproducir archivos MIDI, mensajes exclusivos del sistema
- mensajes MIDI exclusivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904517"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="67616-111">Envío de mensajes de System-Exclusive</span><span class="sxs-lookup"><span data-stu-id="67616-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="67616-112">Los mensajes exclusivos del sistema MIDI son los únicos mensajes MIDI que no caben en un único valor de palabra.</span><span class="sxs-lookup"><span data-stu-id="67616-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="67616-113">Los mensajes exclusivos del sistema pueden tener cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="67616-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="67616-114">Windows proporciona la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensajes exclusivos del sistema a dispositivos de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="67616-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="67616-115">Para especificar los bloques de datos exclusivos del sistema MIDI, use la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="67616-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="67616-116">Después de enviar un bloque de datos exclusivo del sistema mediante **midiOutLongMsg**, debe esperar hasta que el controlador de dispositivo termine con el bloque de datos antes de liberarlo.</span><span class="sxs-lookup"><span data-stu-id="67616-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="67616-117">Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales.</span><span class="sxs-lookup"><span data-stu-id="67616-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="67616-118">Para obtener información sobre las distintas técnicas para supervisar la finalización de bloque de datos, vea [administrar bloques de datos MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="67616-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="67616-119">Cualquier byte de estado de MIDI que no sea un mensaje en tiempo real del sistema finalizará un mensaje exclusivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="67616-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="67616-120">Si está utilizando varios bloques de datos para enviar un único mensaje exclusivo del sistema, no envíe mensajes MIDI que no sean mensajes en tiempo real del sistema entre bloques de datos.</span><span class="sxs-lookup"><span data-stu-id="67616-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 