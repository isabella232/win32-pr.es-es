---
title: Usar una devolución de llamada de evento para administrar la reproducción almacenada en búfer
description: Usar una devolución de llamada de evento para administrar la reproducción almacenada en búfer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Interfaz digital de instrumentos musicales (MIDI), reproducción almacenada en búfer
- MIDI (interfaz digital de instrumentos musicales), reproducción almacenada en búfer
- reproducir archivos MIDI, reproducción almacenada en búfer
- reproducción almacenada en búfer
- CreateEvent (función)
- Interfaz digital de instrumentos musicales (MIDI), devolución de llamada de evento
- MIDI (interfaz digital de instrumentos musicales), devolución de llamada de evento
- reproducir archivos MIDI, devolución de llamada de evento
- devolución de llamada de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790215"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="042ee-112">Usar una devolución de llamada de evento para administrar la reproducción almacenada en búfer</span><span class="sxs-lookup"><span data-stu-id="042ee-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="042ee-113">Para utilizar una devolución de llamada de evento, utilice la función [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar el identificador de un evento.</span><span class="sxs-lookup"><span data-stu-id="042ee-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="042ee-114">En una llamada a la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , especifique \_ el evento de devolución de llamada para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="042ee-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="042ee-115">Después de usar la función [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) , pero antes de enviar eventos MIDI al dispositivo, cree un evento no señalizado mediante una llamada a la función [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , especificando el identificador de eventos recuperado por **CreateEvent**.</span><span class="sxs-lookup"><span data-stu-id="042ee-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="042ee-116">Después, dentro de un bucle que comprueba si el \_ bit Done MHDR está establecido en el miembro **dwFlags** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , use la función [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , especificando el identificador de eventos y un valor de tiempo de espera infinito como parámetros.</span><span class="sxs-lookup"><span data-stu-id="042ee-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="042ee-117">Una devolución de llamada de evento se establece por cualquier cosa que pueda provocar una devolución de llamada de función.</span><span class="sxs-lookup"><span data-stu-id="042ee-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="042ee-118">Dado que las devoluciones de llamada de eventos no reciben notificaciones de cierre, listo o abierto específicas, es posible que una aplicación necesite comprobar el estado del proceso que espera después de que se produzca el evento.</span><span class="sxs-lookup"><span data-stu-id="042ee-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="042ee-119">Es posible que se complete una serie de tareas por la hora que **WaitForSingleObject** devuelve.</span><span class="sxs-lookup"><span data-stu-id="042ee-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 