---
title: Búferes de secuencia
description: Búferes de secuencia
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimedia, búferes de secuencia
- multimedia, búferes de secuencia
- audio multimedia, búferes de secuencia
- audio, búferes de secuencia
- Interfaz digital de instrumentos musicales (MIDI), búferes de secuencia
- MIDI (interfaz digital de instrumentos musicales), búferes de secuencia
- búferes de secuencia, acerca de
- Estructura MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790162"
---
# <a name="stream-buffers"></a>Búferes de secuencia

Las aplicaciones pueden usar búferes de secuencia para enviar flujos de eventos MIDI a un dispositivo. Cada búfer de secuencia es un bloque de memoria al que apunta una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) . Este bloque de memoria contiene datos para uno o más eventos MIDI, cada uno de los cuales se define mediante una estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Una aplicación controla el búfer mediante una llamada a las funciones de manipulación de secuencias, como [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)y [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Formato de búfer de secuencia](stream-buffer-format.md)
-   [Información de tiempo](timing-information.md)
-   [Tipos de eventos MIDI](midi-event-types.md)
-   [Flujos MIDI](midi-streams.md)

 

 