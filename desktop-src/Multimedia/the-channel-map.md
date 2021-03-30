---
title: Asignación de canal
description: Asignación de canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapa de canales
- mapa de canal
- Asignador de MIDI, mensajes de canal
- Mensajes del canal MIDI
- mensajes de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148828"
---
# <a name="the-channel-map"></a>Asignación de canal

La asignación de canal afecta a todos los mensajes del canal MIDI. Los mensajes del canal MIDI incluyen los mensajes de Nota: on, note-off, polyphonic-Key-aftertouch, control-Change, Program-Change, Channel-aftertouch y Pitch-Bend-Change. El asignador de MIDI utiliza un mapa de canal único con una entrada para cada uno de los 16 canales MIDI. Cada entrada de asignación de canal especifica lo siguiente:

-   Un canal de destino para el mensaje MIDI
-   Un dispositivo de salida de destino para el mensaje MIDI
-   Una asignación de revisión opcional que especifica otras modificaciones posibles para el mensaje MIDI

El canal de destino se establece en uno de los 16 canales MIDI. Los mensajes MIDI se modifican para reflejar cada nueva asignación de canal. Por ejemplo, si la entrada de canal de destino para el canal de MIDI 4 está establecida en 6, todos los mensajes MIDI enviados al canal 4 se asignarán al canal 6, tal como se muestra en la siguiente ilustración.

![imagen MIDI asignada](images/mmap-a05.gif)

En este ejemplo, el byte de estado de MIDI 0x93 se asigna a 0x95. El orden inferior de un byte de estado de MIDI especifica el número de canal. Los canales de origen se establecen en activo o inactivo. Los mensajes enviados a los canales de origen inactivos se omiten, por lo que un canal inactivo está en vigor o desactivado.

El dispositivo de salida de destino se establece en uno de los dispositivos de salida MIDI disponibles. Un dispositivo de salida MIDI puede ser un sintetizador interno o un puerto de salida MIDI físico.

Los mensajes del sistema MIDI son mensajes MIDI (con el estado bytes) de 0xF0 a 0xFF. No hay ningún canal asociado a los mensajes del sistema MIDI, por lo que no se pueden asignar. Los mensajes del sistema MIDI se envían a todos los dispositivos de salida MIDI que aparecen en una asignación de canal.

 

 




