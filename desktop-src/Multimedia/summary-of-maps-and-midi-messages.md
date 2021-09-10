---
title: Resumen de los mensajes Mapas y MIDI
description: Resumen de los mensajes Mapas y MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, mapa de canal
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas clave
- mapa del canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371071"
---
# <a name="summary-of-maps-and-midi-messages"></a>Resumen de los mensajes Mapas y MIDI

A continuación se enumeran los bytes de estado de los mensajes DE MIDI y los tipos de mapa que afectan a cada mensaje.



| Estado de MIDI | Descripción               | Tipos de mapas                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Nota desactivada                  | Mapas de canales, mapas de claves   |
| 0x90-0x9F   | Nota sobre                    | Mapas de canales, mapas de claves   |
| 0xA0-0xAF   | Polyphonic-key aftertouch | Mapas de canales, mapas de claves   |
| 0xB0-0xBF   | Control de cambios            | Mapas de canales, mapas de revisiones |
| 0xC0-0xCF   | Cambio del programa            | Mapas de canales, mapas de revisiones |
| 0xD0-0xDF   | Channel aftertouch        | Mapas de canales             |
| 0xE0-0xEF   | Cambio de tono         | Mapas de canales             |
| 0xF0-0xFF   | Sistema                    | No asignado               |



 

-   Los cuatro bits de orden superior representan el valor de estado. Los cuatro bits de orden bajo representan la información del canal.
-   Los mapas de revisiones solo afectan al controlador 7 (volumen principal).
-   Los mensajes del sistema se envían a todos los dispositivos enumerados en un mapa de canal.

 

 




