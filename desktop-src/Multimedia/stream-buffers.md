---
title: Búferes de secuencia
description: Búferes de secuencia
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimedia, búferes de secuencia
- multimedia, búferes de secuencia
- audio multimedia, búferes de secuencia
- audio, búferes de secuencia
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- búferes de secuencia, acerca de
- Estructura MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790162"
---
# <a name="stream-buffers"></a><span data-ttu-id="5be1f-112">Búferes de secuencia</span><span class="sxs-lookup"><span data-stu-id="5be1f-112">Stream Buffers</span></span>

<span data-ttu-id="5be1f-113">Las aplicaciones pueden usar búferes de secuencia para enviar flujos de eventos MIDI a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5be1f-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="5be1f-114">Cada búfer de secuencia es un bloque de memoria al que apunta una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="5be1f-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="5be1f-115">Este bloque de memoria contiene datos para uno o más eventos MIDI, cada uno de los cuales se define mediante una estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="5be1f-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="5be1f-116">Una aplicación controla el búfer mediante una llamada a las funciones de manipulación de secuencias, como [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)y [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="5be1f-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="5be1f-117">Formato de búfer de secuencia</span><span class="sxs-lookup"><span data-stu-id="5be1f-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="5be1f-118">Información de tiempo</span><span class="sxs-lookup"><span data-stu-id="5be1f-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="5be1f-119">Tipos de eventos MIDI</span><span class="sxs-lookup"><span data-stu-id="5be1f-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="5be1f-120">Flujos MIDI</span><span class="sxs-lookup"><span data-stu-id="5be1f-120">MIDI Streams</span></span>](midi-streams.md)

 

 