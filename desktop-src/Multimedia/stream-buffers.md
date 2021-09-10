---
title: Búferes de flujo
description: Búferes de flujo
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimedia, búferes de secuencia
- multimedia, búferes de secuencia
- audio multimedia, búferes de secuencia
- audio, búferes de secuencia
- Interfaz digital de instrumentar música (MIDI), búferes de flujo
- MIDI (Interfaz digital de instrumentar música), búferes de flujo
- búferes de flujo, acerca de
- Estructura DE MIDIHDR
- Estructura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371041"
---
# <a name="stream-buffers"></a>Búferes de flujo

Las aplicaciones pueden usar búferes de flujo para enviar secuencias de eventos DE MIDI a un dispositivo. Cada búfer de secuencia es un bloque de memoria al que apunta [**una estructura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) Este bloque de memoria contiene datos para uno o varios eventos MIDI, cada uno de los cuales está definido por una [**estructura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) Una aplicación controla el búfer mediante una llamada a las funciones de manipulación de secuencias, como [**midiStreamOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen) [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)y [**midiStreamClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)

-   [Formato de búfer de flujo](stream-buffer-format.md)
-   [Información de control de tiempo](timing-information.md)
-   [Tipos de eventos DE MIDI](midi-event-types.md)
-   [Secuencias DE MIDI](midi-streams.md)

 

 