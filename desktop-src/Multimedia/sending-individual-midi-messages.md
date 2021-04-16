---
title: Envío de mensajes MIDI individuales
description: Envío de mensajes MIDI individuales
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), mensajes individuales
- MIDI (interfaz digital de instrumentos musicales), mensajes individuales
- reproducir archivos MIDI, mensajes individuales
- mensajes MIDI individuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665789"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="2b3b8-111">Envío de mensajes MIDI individuales</span><span class="sxs-lookup"><span data-stu-id="2b3b8-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="2b3b8-112">Puede trabajar con mensajes MIDI individuales mediante las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="2b3b8-113">Value</span><span class="sxs-lookup"><span data-stu-id="2b3b8-113">Value</span></span>                                      | <span data-ttu-id="2b3b8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2b3b8-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b3b8-115">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="2b3b8-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="2b3b8-116">Envía un búfer de datos MIDI al dispositivo de salida MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="2b3b8-117">Utilice esta función para enviar mensajes exclusivos del sistema a un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="2b3b8-118">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="2b3b8-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="2b3b8-119">Desactiva todas las notas en todos los canales de un dispositivo de salida MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="2b3b8-120">Los búferes de secuencia y los búferes exclusivos del sistema pendientes se marcan como terminados y se devuelven a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="2b3b8-121">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="2b3b8-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="2b3b8-122">Envía un mensaje MIDI a un dispositivo de salida MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3b8-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="2b3b8-123">Para enviar cualquier mensaje MIDI (excepto para los mensajes exclusivos del sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span><span class="sxs-lookup"><span data-stu-id="2b3b8-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 