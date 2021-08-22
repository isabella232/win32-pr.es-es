---
title: Mapa del canal
description: Mapa del canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, mapa de canal
- mapa del canal
- Asignador de MIDI, mensajes de canal
- Mensajes de canal DE MES
- mensajes de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d514b5af6df6426db7cc5a313d1c6a52070a49c22a8a04e8cd2a9c34f49d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688295"
---
# <a name="the-channel-map"></a>Mapa del canal

El mapa del canal afecta a todos los mensajes de canal DE MES. Los mensajes del canal MIDI incluyen los mensajes note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch y pitch-org-change. El asignador de MIDI usa un mapa de canal único con una entrada para cada uno de los 16 canales DE MIDI. Cada entrada de channel-map especifica lo siguiente:

-   Un canal de destino para el mensaje MIDI
-   Un dispositivo de salida de destino para el mensaje MIDI
-   Un mapa de revisión opcional que especifica otras modificaciones posibles para el mensaje MIDI

El canal de destino se establece en uno de los 16 canales DE MIDI. Los mensajes MIDI se modifican para reflejar cada nueva asignación de canal. Por ejemplo, si la entrada del canal de destino para el canal 4 de MIDI se establece en 6, todos los mensajes MIDI enviados al canal 4 se asignarán al canal 6, como se muestra en la ilustración siguiente.

![imagen de midi asignada](images/mmap-a05.gif)

En este ejemplo, el byte de estado DE 0X93 se asigna a 0x95. El orden bajo de un byte de estado DE MIDI especifica el número de canal. Los canales de origen se establecen en activo o inactivo. Los mensajes enviados a canales de origen inactivos se omiten, por lo que un canal inactivo está en vigor muted o desactivado.

El dispositivo de salida de destino se establece en uno de los dispositivos de salida DE MIDI disponibles. Un dispositivo de salida de MIDI puede ser un sintetizador interno o un puerto de salida DE MIDI físico.

Los mensajes del sistema MIDI son mensajes MIDI (con bytes de estado) 0xF0 a 0xFF. No hay ningún canal asociado a los mensajes del sistema MIDI, por lo que no se pueden asignar. Los mensajes del sistema MIDI se envían a todos los dispositivos de salida DE MIDI enumerados en un mapa de canales.

 

 




