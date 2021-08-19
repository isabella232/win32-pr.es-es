---
title: Usar una ventana o un subproceso para administrar la reproducción en búfer
description: Usar una ventana o un subproceso para administrar la reproducción en búfer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Interfaz digital instrumentada (MIDI), reproducción en búfer
- MIDI (Interfaz digital instrumentada), reproducción en búfer
- reproducir archivos MIDI, reproducción en búfer
- reproducción en búfer
- MM_MOM_CLOSE mensaje
- MM_MOM_DONE mensaje
- MM_MOM_OPEN mensaje
- Interfaz digital instrumentable (MIDI), envío de mensajes
- MIDI (Interfaz digital instrumenta instrumentable), envío de mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc0acb39090a640d60539542a439111287faef246adf64aef7ee12ced3ae09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801259"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Usar una ventana o un subproceso para administrar la reproducción en búfer

Los mensajes siguientes se pueden enviar a una ventana o subproceso para administrar la reproducción de mensajes o búferes de flujo exclusivos del sistema DE MIDI.



| Valor                                  | Significado                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ CLOSE**](mm-mom-close.md) | Se envía cuando el dispositivo se cierra mediante la [**función midiOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)                                                                               |
| [**MM \_ MOM \_ DONE**](mm-mom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante [**la función midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**o midiStreamOut.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) |
| [**MM \_ MOM \_ OPEN**](mm-mom-open.md)   | Se envía cuando se abre el dispositivo mediante la [**función midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)                                                                                 |



 

Un *parámetro wParam* y *un parámetro lParam* están asociados a cada uno de estos mensajes. El *parámetro wParam* siempre especifica el identificador de un dispositivo MIDI abierto. Para [**MM \_ MOM \_ DONE**](mm-mom-done.md), *lParam especifica* una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el bloque de datos completado. El *parámetro lParam* no se usa para [**MM MOM \_ \_ CLOSE**](mm-mom-close.md) y [**MM MOM \_ \_ OPEN**](mm-mom-open.md).

El mensaje más útil probablemente sea MM \_ MOM \_ DONE. A menos que necesite asignar memoria o inicializar variables, probablemente no necesite procesar MM \_ MOM OPEN y MM MOM \_ \_ \_ CLOSE. Una vez completada la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos.

 

 