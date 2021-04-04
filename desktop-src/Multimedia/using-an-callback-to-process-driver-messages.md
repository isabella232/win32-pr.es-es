---
title: Usar una devolución de llamada de evento para procesar mensajes de controlador
description: Usar una devolución de llamada de evento para procesar mensajes de controlador
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio de onda, devolución de llamada de evento
- bloques de datos de audio, devolución de llamada de evento
- audio de forma de onda, procesamiento de mensajes de controlador
- bloques de datos de audio, procesar mensajes de controlador
- procesar mensajes de controlador
- CreateEvent (función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790210"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="22029-109">Usar una devolución de llamada de evento para procesar mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="22029-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="22029-110">Para utilizar una devolución de llamada de evento, utilice la función [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para crear un evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="22029-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="22029-111">En la llamada a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , especifique **el \_ evento de devolución de llamada** para el parámetro *fdwOpen* .</span><span class="sxs-lookup"><span data-stu-id="22029-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="22029-112">Después de llamar a la función [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , pero antes de enviar datos de audio de forma de onda al dispositivo, coloque el evento en un estado no señalizado mediante una llamada a la función [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) .</span><span class="sxs-lookup"><span data-stu-id="22029-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="22029-113">Después, dentro de un bucle que comprueba si la marca de **WHDR \_ Done** está establecida en el miembro **DwFlags** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , llame a la función [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) y especifique como parámetros el identificador de evento y un valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="22029-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="22029-114">Dado que las devoluciones de llamada de eventos no reciben notificaciones de cierre, listo o abierto específicas, es posible que una aplicación tenga que comprobar el estado del proceso que espera después de que se produzca el evento.</span><span class="sxs-lookup"><span data-stu-id="22029-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="22029-115">Es posible que se haya completado una serie de tareas en el momento en que se devuelve [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="22029-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22029-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22029-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22029-117">Bloques de datos de audio</span><span class="sxs-lookup"><span data-stu-id="22029-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 