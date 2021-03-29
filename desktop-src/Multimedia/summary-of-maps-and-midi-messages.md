---
title: Resumen de mapas y mensajes MIDI
description: Resumen de mapas y mensajes MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapa de canales
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas de claves
- mapa de canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778840"
---
# <a name="summary-of-maps-and-midi-messages"></a>Resumen de mapas y mensajes MIDI

A continuación se indican los bytes de estado de los mensajes MIDI y los tipos de mapa que afectan a cada mensaje.



| Estado de MIDI | Descripción               | Tipos de asignación                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Nota OFF                  | Mapas de canales, mapas de claves   |
| 0x90-0x9F   | Nota sobre                    | Mapas de canales, mapas de claves   |
| 0xA0-0xAF   | Polyphonic-clave aftertouch | Mapas de canales, mapas de claves   |
| 0xB0-0xBF   | Cambio de control            | Mapas de canales, mapas de revisiones |
| 0xC0-0xCF   | Cambio de programa            | Mapas de canales, mapas de revisiones |
| 0xD0-0xDF   | Canal aftertouch        | Mapas de canal             |
| 0xE0-0xEF   | Cambio de plegado de tono         | Mapas de canal             |
| 0xF0-0xFF   | System                    | No asignado               |



 

-   Los cuatro bits de orden superior representan el valor de estado. Los cuatro bits de orden inferior representan la información del canal.
-   Las asignaciones de revisión solo afectan al controlador 7 (volumen principal).
-   Los mensajes del sistema se envían a todos los dispositivos que aparecen en una asignación de canal.

 

 




