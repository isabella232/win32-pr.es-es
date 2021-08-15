---
title: Usar una devolución de llamada de eventos para administrar la reproducción en búfer
description: Usar una devolución de llamada de eventos para administrar la reproducción en búfer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Interfaz digital de instrumentar música (MIDI), reproducción en búfer
- MIDI (Interfaz digital instrumentada), reproducción en búfer
- reproducir archivos MIDI, reproducción en búfer
- reproducción en búfer
- Función CreateEvent
- Interfaz digital de instrumentar música (MIDI), devolución de llamada de eventos
- MIDI (Interfaz digital de instrumentar música), devolución de llamada de eventos
- reproducir archivos MIDI, devolución de llamada de eventos
- devolución de llamada de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747652c10471662daacfe433a8fc22d5248bf2fe2365b6b314e76d0b91ced127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370271"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Usar una devolución de llamada de eventos para administrar la reproducción en búfer

Para usar una devolución de llamada de evento, use [la función CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar el identificador de un evento. En una llamada a la [**función midiOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) especifique CALLBACK \_ EVENT para el parámetro *dwFlags.* Después de usar la función [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) pero antes de enviar eventos MIDI al dispositivo, cree un evento sin signo llamando a la [función ResetEvent,](/windows/win32/api/synchapi/nf-synchapi-resetevent) especificando el identificador de evento recuperado por **CreateEvent**. A continuación, dentro de un bucle que comprueba si el bit de MHDR DONE está establecido en el miembro dwFlags de la estructura \_ [**MIDIHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) use la función [WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) especificando el identificador del evento y un valor de tiempo de espera de INFINITE como parámetros. 

Cualquier elemento que pueda provocar una devolución de llamada de función establece una devolución de llamada de evento.

Dado que las devoluciones de llamada de eventos no reciben notificaciones específicas de cierre, realización o apertura, es posible que una aplicación tenga que comprobar el estado del proceso que está esperando después de que se produzca el evento. Es posible que se puedan completar varias tareas en el momento en que **waitForSingleObject devuelve** .

 

 