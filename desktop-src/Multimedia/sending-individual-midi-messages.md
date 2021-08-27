---
title: Envío de mensajes INDIVIDUALES DE MIDI
description: Envío de mensajes INDIVIDUALES DE MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital de instrumentar música), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentar música (MIDI), mensajes individuales
- MIDI (Interfaz digital de instrumentar música), mensajes individuales
- reproducir archivos MIDI, mensajes individuales
- mensajes individuales de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037455"
---
# <a name="sending-individual-midi-messages"></a>Envío de mensajes INDIVIDUALES DE MIDI

Puede trabajar con mensajes MIDI individuales mediante las siguientes funciones.



| Value                                      | Significado                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envía un búfer de datos DE MIDI al dispositivo de salida DE MIDI especificado. Use esta función para enviar mensajes exclusivos del sistema a un dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Desactiva todas las notas de todos los canales para un dispositivo de salida DE MIDI especificado. Los búferes exclusivos del sistema y los búferes de secuencia pendientes se marcan como hechos y se devuelven a la aplicación. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envía un mensaje MIDI a un dispositivo de salida DE MIDI especificado.                                                                                                                             |



 

Para enviar cualquier mensaje MIDI (excepto para los mensajes exclusivos del sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 