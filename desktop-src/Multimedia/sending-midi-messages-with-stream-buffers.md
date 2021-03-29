---
title: Envío de mensajes MIDI con búferes de secuencia
description: Envío de mensajes MIDI con búferes de secuencia
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- reproducir archivos MIDI, búferes de secuencia
- búferes de secuencia, envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790168"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="af7bd-111">Envío de mensajes MIDI con búferes de secuencia</span><span class="sxs-lookup"><span data-stu-id="af7bd-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="af7bd-112">Cuando la aplicación trabaja con búferes de secuencia, usa la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todos los mensajes MIDI (cortos y largos) al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af7bd-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="af7bd-113">Para especificar los bloques de datos de la secuencia, use las estructuras [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) y [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="af7bd-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="af7bd-114">La estructura **MIDIHDR** contiene una dirección de un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas asordenas.</span><span class="sxs-lookup"><span data-stu-id="af7bd-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="af7bd-115">Los datos se almacenan en forma de estructuras **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="af7bd-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="af7bd-116">El sistema impone un límite de tamaño de 64 k en los búferes de secuencia.</span><span class="sxs-lookup"><span data-stu-id="af7bd-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="af7bd-117">Después de utilizar **midiStreamOut** para enviar un búfer de flujo de datos, debe esperar hasta que el controlador de dispositivo termine con el bloque de datos antes de liberarlo.</span><span class="sxs-lookup"><span data-stu-id="af7bd-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="af7bd-118">Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales.</span><span class="sxs-lookup"><span data-stu-id="af7bd-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="af7bd-119">Para obtener información sobre las distintas técnicas para supervisar la finalización de bloque de datos, vea [administrar bloques de datos MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="af7bd-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 