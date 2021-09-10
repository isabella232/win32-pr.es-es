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
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371006"
---
# <a name="sending-individual-midi-messages"></a>Envío de mensajes INDIVIDUALES DE MIDI

Puede trabajar con mensajes MIDI individuales mediante las siguientes funciones.



| Value                                      | Significado                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envía un búfer de datos DE MIDI al dispositivo de salida DE MIDI especificado. Use esta función para enviar mensajes exclusivos del sistema a un dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Desactiva todas las notas de todos los canales para un dispositivo de salida DE MIDI especificado. Los búferes exclusivos del sistema y los búferes de secuencia pendientes se marcan como hechos y se devuelven a la aplicación. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envía un mensaje MIDI a un dispositivo de salida DE MIDI especificado.                                                                                                                             |



 

Para enviar cualquier mensaje MIDI (excepto para los mensajes exclusivos del sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 