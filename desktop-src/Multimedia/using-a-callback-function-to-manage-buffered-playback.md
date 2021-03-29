---
title: Usar una función de devolución de llamada para administrar la reproducción almacenada en búfer
description: Usar una función de devolución de llamada para administrar la reproducción almacenada en búfer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Interfaz digital de instrumentos musicales (MIDI), reproducción almacenada en búfer
- MIDI (interfaz digital de instrumentos musicales), reproducción almacenada en búfer
- reproducir archivos MIDI, reproducción almacenada en búfer
- reproducción almacenada en búfer
- Mensaje MOM_CLOSE
- Mensaje MOM_DONE
- Mensaje MOM_OPEN
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), funciones de devolución de llamada
- MIDI (interfaz digital de instrumentos musicales), funciones de devolución de llamada
- reproducir archivos MIDI, funciones de devolución de llamada
- Función de devolución de llamada MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790870"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="a0263-118">Usar una función de devolución de llamada para administrar la reproducción almacenada en búfer</span><span class="sxs-lookup"><span data-stu-id="a0263-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="a0263-119">Puede definir su propia función de devolución de llamada para administrar la reproducción almacenada en búfer de dispositivos de salida MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0263-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="a0263-120">La función de devolución de llamada se documenta como [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0263-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="a0263-121">Los siguientes mensajes se pueden enviar al parámetro *wMsg* de la función de devolución de llamada **MidiOutProc** .</span><span class="sxs-lookup"><span data-stu-id="a0263-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="a0263-122">Value</span><span class="sxs-lookup"><span data-stu-id="a0263-122">Value</span></span>                           | <span data-ttu-id="a0263-123">Significado</span><span class="sxs-lookup"><span data-stu-id="a0263-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0263-124">**cierre de MOM \_**</span><span class="sxs-lookup"><span data-stu-id="a0263-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="a0263-125">Se envía cuando el dispositivo se cierra con la función [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="a0263-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="a0263-126">**MOM \_ Done**</span><span class="sxs-lookup"><span data-stu-id="a0263-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="a0263-127">Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="a0263-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="a0263-128">**abierto de MOM \_**</span><span class="sxs-lookup"><span data-stu-id="a0263-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="a0263-129">Se envía cuando el dispositivo se abre con la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="a0263-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="a0263-130">Estos mensajes son similares a los enviados a las funciones de procedimiento de ventana, pero los parámetros son diferentes.</span><span class="sxs-lookup"><span data-stu-id="a0263-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="a0263-131">Un identificador del dispositivo MIDI abierto se pasa como un parámetro a la función de devolución de llamada, junto con la palabra de datos de instancia pasados mediante **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="a0263-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="a0263-132">Una vez que el controlador termina con un bloque de datos, puede limpiar y liberar el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="a0263-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="a0263-133">Debido a las restricciones sugeridas en las funciones de devolución de llamada, es mejor no hacerlo desde la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a0263-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 