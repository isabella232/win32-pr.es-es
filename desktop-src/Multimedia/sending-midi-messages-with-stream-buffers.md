---
title: Envío de mensajes MIDI con búferes de secuencia
description: Envío de mensajes MIDI con búferes de secuencia
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Interfaz digital de instrumentar música (MIDI), búferes de flujo
- MIDI (Interfaz digital de instrumentar música), búferes de flujo
- reproducir archivos MIDI, búferes de secuencia
- búferes de flujo, envío de mensajes MIDI
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital de instrumentar música), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ab8fd8d09295cc40a3ea9b5d8070603a4e7813030b4f04f92a51f7f8709f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892735"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Envío de mensajes MIDI con búferes de secuencia

Cuando la aplicación funciona con búferes de flujo, usa la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todos los mensajes (cortos y largos) DE MIDI al dispositivo. Para especificar bloques de datos de flujo, use las estructuras [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) [**y MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) La **estructura MIDIHDR** contiene una dirección de un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas de la organización. Los datos se almacenan en forma de estructuras **MIDIEVENT.** El sistema impone un límite de tamaño de 64 000 en búferes de flujo.

Después de usar **midiStreamOut para** enviar un búfer de flujo de datos, debe esperar hasta que el controlador del dispositivo finalice con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloques de datos, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

 

 