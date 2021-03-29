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
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Usar una ventana o subproceso para administrar la reproducción almacenada en búfer

Los siguientes mensajes se pueden enviar a una ventana o subproceso para administrar la reproducción de mensajes o búferes de secuencia exclusivos del sistema MIDI.



| Value                                  | Significado                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cierre de MM \_ MOM \_**](mm-mom-close.md) | Se envía cuando el dispositivo se cierra con la función [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MM \_ MOM \_ listo**](mm-mom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**MM \_ MOM \_ abierto**](mm-mom-open.md)   | Se envía cuando el dispositivo se abre con la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Un parámetro *wParam* y un parámetro *lParam* están asociados a cada uno de estos mensajes. El parámetro *wParam* siempre especifica el identificador de un dispositivo MIDI abierto. Para [**mm \_ MOM \_ Done**](mm-mom-done.md), *lParam* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el bloque de datos completado. El parámetro *lParam* no se usa para [**el \_ \_ cierre de mm MOM**](mm-mom-close.md) y el de [**mm para \_ \_ Open**](mm-mom-open.md).

El mensaje más útil es probablemente MM \_ MOM \_ done. A menos que necesite asignar memoria o inicializar variables, es probable que no necesite procesar MM \_ MOM \_ Open y mm \_ MOM \_ Close. Cuando se completa la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos.

 

 