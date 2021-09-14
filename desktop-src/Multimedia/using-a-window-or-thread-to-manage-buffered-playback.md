---
title: Usar una ventana o un subproceso para administrar la reproducción en búfer
description: Usar una ventana o un subproceso para administrar la reproducción en búfer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Interfaz digital de instrumentar música (MIDI), reproducción en búfer
- MIDI (Interfaz digital instrumentada), reproducción en búfer
- reproducir archivos MIDI, reproducción en búfer
- reproducción en búfer
- MM_MOM_CLOSE mensaje
- MM_MOM_DONE mensaje
- MM_MOM_OPEN mensaje
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital de instrumentar música), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245793"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Usar una ventana o un subproceso para administrar la reproducción en búfer

Los mensajes siguientes se pueden enviar a una ventana o subproceso para administrar la reproducción de mensajes exclusivos del sistema o búferes de secuencia de MIDI.



| Value                                  | Significado                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ CLOSE**](mm-mom-close.md) | Se envía cuando el dispositivo se cierra mediante la [**función midiOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)                                                                               |
| [**MM \_ MOM \_ DONE**](mm-mom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la [**función midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**o midiStreamOut.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) |
| [**MM \_ MOM \_ OPEN**](mm-mom-open.md)   | Se envía cuando se abre el dispositivo mediante la [**función midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)                                                                                 |



 

Un *parámetro wParam* y un *parámetro lParam* están asociados a cada uno de estos mensajes. El *parámetro wParam* siempre especifica el identificador de un dispositivo MIDI abierto. Para [**MM \_ MOM \_ DONE**](mm-mom-done.md), *lParam* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el bloque de datos completado. El *parámetro lParam* no se usa para [**MM MOM \_ \_ CLOSE**](mm-mom-close.md) y [**MM MOM \_ \_ OPEN.**](mm-mom-open.md)

El mensaje más útil probablemente sea MM \_ MOM \_ DONE. A menos que necesite asignar memoria o inicializar variables, es probable que no necesite procesar MM \_ MOM OPEN y MM MOM \_ \_ \_ CLOSE. Una vez completada la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos.

 

 