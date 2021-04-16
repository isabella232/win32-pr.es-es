---
title: Envío de mensajes MIDI individuales
description: Envío de mensajes MIDI individuales
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), mensajes individuales
- MIDI (interfaz digital de instrumentos musicales), mensajes individuales
- reproducir archivos MIDI, mensajes individuales
- mensajes MIDI individuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665789"
---
# <a name="sending-individual-midi-messages"></a>Envío de mensajes MIDI individuales

Puede trabajar con mensajes MIDI individuales mediante las siguientes funciones.



| Value                                      | Significado                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envía un búfer de datos MIDI al dispositivo de salida MIDI especificado. Utilice esta función para enviar mensajes exclusivos del sistema a un dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Desactiva todas las notas en todos los canales de un dispositivo de salida MIDI especificado. Los búferes de secuencia y los búferes exclusivos del sistema pendientes se marcan como terminados y se devuelven a la aplicación. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envía un mensaje MIDI a un dispositivo de salida MIDI especificado.                                                                                                                             |



 

Para enviar cualquier mensaje MIDI (excepto para los mensajes exclusivos del sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 