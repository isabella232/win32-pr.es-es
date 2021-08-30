---
title: Usar una función de devolución de llamada para administrar la reproducción en búfer
description: Usar una función de devolución de llamada para administrar la reproducción en búfer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Interfaz digital instrumentada (MIDI), reproducción en búfer
- MIDI (Interfaz digital instrumentada), reproducción en búfer
- reproducir archivos MIDI, reproducción en búfer
- reproducción en búfer
- MOM_CLOSE mensaje
- MOM_DONE mensaje
- MOM_OPEN mensaje
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital instrumenta de música), envío de mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital instrumentable (MIDI), funciones de devolución de llamada
- FUNCIONES DE DEVOLUCIÓN DE LLAMADA (Interfaz digital instrumenta instrumentable), funciones de devolución de llamada
- reproducir archivos MIDI, funciones de devolución de llamada
- Función de devolución de llamada de MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727474e5323519cb5f70dbcaa71798c41a8c6f9433852718051a8584a2967e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804695"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Usar una función de devolución de llamada para administrar la reproducción en búfer

Puede definir su propia función de devolución de llamada para administrar la reproducción en búfer de los dispositivos de salida DE MIDI. La función de devolución de llamada se documenta [**como MidiOutProc**](/previous-versions//dd798478(v=vs.85)).

Los mensajes siguientes se pueden enviar al parámetro *wMsg* de la función de devolución de llamada **MidiOutProc.**



| Valor                           | Significado                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MOM \_ CLOSE**](mom-close.md) | Se envía cuando el dispositivo se cierra mediante la [**función midiOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)                                                                               |
| [**MOM \_ DONE**](mom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante [**la función midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**o midiStreamOut.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) |
| [**MOM \_ OPEN**](mom-open.md)   | Se envía cuando se abre el dispositivo mediante la [**función midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)                                                                                 |



 

Estos mensajes son similares a los enviados a funciones de procedimiento de ventana, pero los parámetros son diferentes. Un identificador del dispositivo MIDI abierto se pasa como parámetro a la función de devolución de llamada, junto con la palabra doble de los datos de instancia pasados **mediante midiOutOpen**.

Una vez finalizado el controlador con un bloque de datos, puede limpiar y liberar el bloque de datos. Debido a las restricciones sugeridas en las funciones de devolución de llamada, es mejor no hacerlo desde dentro de la función de devolución de llamada.

 

 