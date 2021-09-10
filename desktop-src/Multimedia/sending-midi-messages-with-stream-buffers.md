---
title: Envío de mensajes MIDI con búferes de secuencia
description: Envío de mensajes MIDI con búferes de secuencia
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Interfaz digital instrumentable (MIDI), búferes de secuencia
- MIDI (Interfaz digital instrumenta de música), búferes de secuencia
- reproducir archivos MIDI, búferes de secuencia
- búferes de flujo, envío de mensajes MIDI
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital instrumenta instrumentable), envío de mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371011"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Envío de mensajes MIDI con búferes de secuencia

Cuando la aplicación funciona con búferes de flujo, usa la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todos los mensajes (cortos y largos) DE MIDI al dispositivo. Para especificar bloques de datos de flujo, use [**las estructuras MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) [**y MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) La **estructura MIDIHDR** contiene una dirección de un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas variadas. Los datos se almacenan en forma de estructuras **DE MIDIEVENT.** El sistema impone un límite de tamaño de 64 000 en búferes de flujo.

Después de usar **midiStreamOut para** enviar un búfer de flujo de datos, debe esperar hasta que el controlador de dispositivo finalice con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloques de datos, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

 

 