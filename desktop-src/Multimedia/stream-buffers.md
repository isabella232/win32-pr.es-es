---
title: Búferes de flujo
description: Búferes de flujo
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimedia, búferes de secuencia
- multimedia, búferes de secuencia
- audio multimedia, búferes de secuencia
- audio, búferes de secuencia
- Interfaz digital instrumentable (MIDI), búferes de secuencia
- MIDI (Interfaz digital instrumenta de música), búferes de secuencia
- búferes de flujo, acerca de
- Estructura DE MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac10d024089a856880097c5d87ae501d62655f858030535ff4128f1fd9d31447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037075"
---
# <a name="stream-buffers"></a>Búferes de flujo

Las aplicaciones pueden usar búferes de flujo para enviar secuencias de eventos DE MIDI a un dispositivo. Cada búfer de flujo es un bloque de memoria al que apunta una [**estructura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) Este bloque de memoria contiene datos para uno o varios eventos MIDI, cada uno de los cuales se define mediante una [**estructura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) Una aplicación controla el búfer mediante una llamada a las funciones de manipulación de secuencias, como [**midiStreamOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen) [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)y [**midiStreamClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)

-   [Formato de búfer de secuencia](stream-buffer-format.md)
-   [Información de tiempo](timing-information.md)
-   [Tipos de eventos MIDI](midi-event-types.md)
-   [Secuencias DE MIDI](midi-streams.md)

 

 