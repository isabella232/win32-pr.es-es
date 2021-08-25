---
title: Asignador de MIDI
description: Asignador de MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimedia, asignador DE MES
- multimedia, asignador DE MES
- audio multimedia, Asignador DE NOTAS
- audio,Asignador DE AUDIO
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, acerca de
- Asignador de MIDI, origen
- Asignador de MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5becc117668964a584f29c311c3e3ac477f672085e837e28d7eecc595658d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805105"
---
# <a name="the-midi-mapper"></a>Asignador de MIDI

Los servicios de revisión estándar del asignador de MIDI proporcionan la reproducción de archivos MIDI independientes del dispositivo para las aplicaciones. El asignador de MIDI se puede usar con el secuenciador MCI MIDI o con servicios de salida DE BAJA NIVEL DE MIDI.

A menos que se indique lo contrario, todas las referencias a los números de canal MIDI usan los números de canal lógico del 1 al 16. Estos números de canal lógico corresponden a los números de canal físicos del 0 al 15 que realmente forman parte del mensaje MIDI. Todas las referencias a los valores de cambio de programa y clave de MIDI usan los valores físicos de 0 a 127. Todos los números son decimales a menos que estén precedidos de un prefijo "0x", en cuyo caso son hexadecimales.

En la explicación del asignador de MIDI, el término *source* hace referencia al lado de entrada del asignador DE MIDI. El término *destino* hace referencia al lado de salida del asignador de MIDI. Por ejemplo, un canal de origen es el canal MIDI de un mensaje enviado al asignador DE MIDI, y un canal de destino es el canal MIDI de un mensaje enviado desde el Asignador DE MIDI a un dispositivo de salida.

-   [Asignador y Windows](the-midi-mapper-and-windows.md)
-   [Arquitectura del asignador de MIDI](the-midi-mapper-architecture.md)
-   [Mapa del canal](the-channel-map.md)
-   [Aplicación de Mapas](patch-maps.md)
-   [Escalar de volumen](the-volume-scalar.md)
-   [Clave Mapas](key-maps.md)
-   [Resumen de los mensajes Mapas y MIDI](summary-of-maps-and-midi-messages.md)

 

 




