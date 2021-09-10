---
title: Mapa de canal
description: Mapa de canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital instrumenta instrumenta),Asignador DE MIDI
- Asignador de MIDI, mapa de canal
- channel map
- Asignador de MIDI, mensajes de canal
- Mensajes de canal MIDI
- mensajes de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371066"
---
# <a name="the-channel-map"></a>Mapa de canal

El mapa de canal afecta a todos los mensajes de canal DE MED. Los mensajes del canal MIDI incluyen los mensajes note-on, note-off, polyfónic-key-aftertouch, control-change, program-change, channel-aftertouch y pitch-ctrl-change. El Asignador de MIDI usa un mapa de canal único con una entrada para cada uno de los 16 canales DE MIDI. Cada entrada de mapa de canal especifica lo siguiente:

-   Un canal de destino para el mensaje DE MIDI
-   Un dispositivo de salida de destino para el mensaje MIDI
-   Un mapa de revisión opcional que especifica otras modificaciones posibles para el mensaje DE MIDI

El canal de destino se establece en uno de los 16 canales DE MIDI. Los mensajes DE MIDI se modifican para reflejar cada nueva asignación de canal. Por ejemplo, si la entrada del canal de destino para el canal MIDI 4 se establece en 6, todos los mensajes DE MIDI enviados al canal 4 se asignarán al canal 6, como se muestra en la ilustración siguiente.

![imagen de midi asignada](images/mmap-a05.gif)

En este ejemplo, el byte de estado de MIDI 0x93 asigna a 0x95. El orden bajo de un byte de estado DE MIDI especifica el número de canal. Los canales de origen se establecen en activo o inactivo. Los mensajes enviados a canales de origen inactivos se omiten, por lo que un canal inactivo está en vigor muted o desactivado.

El dispositivo de salida de destino se establece en uno de los dispositivos de salida DE MIDI disponibles. Un dispositivo de salida DE MIDI puede ser un sintetizador interno o un puerto de salida DE MIDI físico.

Los mensajes del sistema MIDI son mensajes MIDI (con bytes de estado) 0xF0 a 0xFF. No hay ningún canal asociado a los mensajes del sistema MIDI, por lo que no se pueden asignar. Los mensajes del sistema MIDI se envían a todos los dispositivos de salida DE MIDI enumerados en un mapa de canal.

 

 




