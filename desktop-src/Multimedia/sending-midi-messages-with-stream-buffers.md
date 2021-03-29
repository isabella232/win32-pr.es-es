---
title: Envío de mensajes MIDI con búferes de secuencia
description: Envío de mensajes MIDI con búferes de secuencia
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- reproducir archivos MIDI, búferes de secuencia
- búferes de secuencia, envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790168"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Envío de mensajes MIDI con búferes de secuencia

Cuando la aplicación trabaja con búferes de secuencia, usa la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todos los mensajes MIDI (cortos y largos) al dispositivo. Para especificar los bloques de datos de la secuencia, use las estructuras [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) y [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . La estructura **MIDIHDR** contiene una dirección de un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas asordenas. Los datos se almacenan en forma de estructuras **MIDIEVENT** . El sistema impone un límite de tamaño de 64 k en los búferes de secuencia.

Después de utilizar **midiStreamOut** para enviar un búfer de flujo de datos, debe esperar hasta que el controlador de dispositivo termine con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloque de datos, vea [administrar bloques de datos MIDI](managing-midi-data-blocks.md).

 

 