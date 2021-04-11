---
title: El asignador MIDI
description: El asignador MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimedia, asignador MIDI
- multimedia, asignador MIDI
- audio multimedia, asignador MIDI
- audio, asignador MIDI
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, acerca de
- Asignador MIDI, origen
- Asignador de MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075548"
---
# <a name="the-midi-mapper"></a>El asignador MIDI

Los servicios de revisión estándar del asignador MIDI proporcionan la reproducción de archivos MIDI independientes del dispositivo para las aplicaciones. El asignador MIDI se puede usar con el secuenciador MIDI de MCI o con los servicios de salida MIDI de bajo nivel.

A menos que se indique lo contrario, todas las referencias a números de canal MIDI usan los números de canal lógico del 1 al 16. Estos números de canal lógico se corresponden con los números de canal físico del 0 al 15 que, en realidad, forman parte del mensaje MIDI. Todas las referencias a los valores de clave y cambio de programa MIDI usan los valores físicos del 0 al 127. Todos los números son decimales a menos que estén precedidos por el prefijo "0x", en cuyo caso son hexadecimales.

En la explicación del Mapeador MIDI, el término *origen* hace referencia al lado de entrada del asignador MIDI. El término *destino* hace referencia al lado de salida del asignador MIDI. Por ejemplo, un canal de origen es el canal MIDI de un mensaje enviado al asignador de MIDI y un canal de destino es el canal MIDI de un mensaje enviado desde el asignador MIDI a un dispositivo de salida.

-   [El asignador de MIDI y Windows](the-midi-mapper-and-windows.md)
-   [Arquitectura del asignador MIDI](the-midi-mapper-architecture.md)
-   [Asignación de canal](the-channel-map.md)
-   [Mapas de revisiones](patch-maps.md)
-   [El volumen escalar](the-volume-scalar.md)
-   [Mapas de claves](key-maps.md)
-   [Resumen de mapas y mensajes MIDI](summary-of-maps-and-midi-messages.md)

 

 




