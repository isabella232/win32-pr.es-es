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
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Usar una función de devolución de llamada para administrar la reproducción almacenada en búfer

Puede definir su propia función de devolución de llamada para administrar la reproducción almacenada en búfer de dispositivos de salida MIDI. La función de devolución de llamada se documenta como [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).

Los siguientes mensajes se pueden enviar al parámetro *wMsg* de la función de devolución de llamada **MidiOutProc** .



| Value                           | Significado                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cierre de MOM \_**](mom-close.md) | Se envía cuando el dispositivo se cierra con la función [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MOM \_ Done**](mom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**abierto de MOM \_**](mom-open.md)   | Se envía cuando el dispositivo se abre con la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Estos mensajes son similares a los enviados a las funciones de procedimiento de ventana, pero los parámetros son diferentes. Un identificador del dispositivo MIDI abierto se pasa como un parámetro a la función de devolución de llamada, junto con la palabra de datos de instancia pasados mediante **midiOutOpen**.

Una vez que el controlador termina con un bloque de datos, puede limpiar y liberar el bloque de datos. Debido a las restricciones sugeridas en las funciones de devolución de llamada, es mejor no hacerlo desde la función de devolución de llamada.

 

 