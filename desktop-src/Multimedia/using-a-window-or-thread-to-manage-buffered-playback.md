---
title: Usar una ventana o subproceso para administrar la reproducción almacenada en búfer
description: Usar una ventana o subproceso para administrar la reproducción almacenada en búfer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Interfaz digital de instrumentos musicales (MIDI), reproducción almacenada en búfer
- MIDI (interfaz digital de instrumentos musicales), reproducción almacenada en búfer
- reproducir archivos MIDI, reproducción almacenada en búfer
- reproducción almacenada en búfer
- Mensaje MM_MOM_CLOSE
- Mensaje MM_MOM_DONE
- Mensaje MM_MOM_OPEN
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358933"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="106a5-114">Usar una ventana o subproceso para administrar la reproducción almacenada en búfer</span><span class="sxs-lookup"><span data-stu-id="106a5-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="106a5-115">Los siguientes mensajes se pueden enviar a una ventana o subproceso para administrar la reproducción de mensajes o búferes de secuencia exclusivos del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="106a5-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="106a5-116">Value</span><span class="sxs-lookup"><span data-stu-id="106a5-116">Value</span></span>                                  | <span data-ttu-id="106a5-117">Significado</span><span class="sxs-lookup"><span data-stu-id="106a5-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="106a5-118">**cierre de MM \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="106a5-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="106a5-119">Se envía cuando el dispositivo se cierra con la función [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="106a5-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="106a5-120">**MM \_ MOM \_ listo**</span><span class="sxs-lookup"><span data-stu-id="106a5-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="106a5-121">Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="106a5-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="106a5-122">**MM \_ MOM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="106a5-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="106a5-123">Se envía cuando el dispositivo se abre con la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="106a5-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="106a5-124">Un parámetro *wParam* y un parámetro *lParam* están asociados a cada uno de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="106a5-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="106a5-125">El parámetro *wParam* siempre especifica el identificador de un dispositivo MIDI abierto.</span><span class="sxs-lookup"><span data-stu-id="106a5-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="106a5-126">Para [**mm \_ MOM \_ Done**](mm-mom-done.md), *lParam* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el bloque de datos completado.</span><span class="sxs-lookup"><span data-stu-id="106a5-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="106a5-127">El parámetro *lParam* no se usa para [**el \_ \_ cierre de mm MOM**](mm-mom-close.md) y el de [**mm para \_ \_ Open**](mm-mom-open.md).</span><span class="sxs-lookup"><span data-stu-id="106a5-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="106a5-128">El mensaje más útil es probablemente MM \_ MOM \_ done.</span><span class="sxs-lookup"><span data-stu-id="106a5-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="106a5-129">A menos que necesite asignar memoria o inicializar variables, es probable que no necesite procesar MM \_ MOM \_ Open y mm \_ MOM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="106a5-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="106a5-130">Cuando se completa la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="106a5-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 