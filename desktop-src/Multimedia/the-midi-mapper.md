---
title: Asignador de MIDI
description: Asignador de MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimedia,Asignador DE MIDI
- multimedia, Asignador de MIDI
- audio multimedia, Asignador de MIDI
- audio,Asignador DE MIDI
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital instrumenta instrumenta),Asignador DE MIDI
- Asignador de MIDI, acerca de
- Asignador de MIDI, origen
- Asignador de MIDI,destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260716"
---
# <a name="the-midi-mapper"></a>Asignador de MIDI

Los servicios de revisión estándar del asignador DE MIDI proporcionan reproducción de archivos MIDI independientes del dispositivo para las aplicaciones. El asignador de MIDI se puede usar con el secuenciador MCI MIDI o con servicios de salida DE MIDI de bajo nivel.

A menos que se indique lo contrario, todas las referencias a los números de canal MIDI usan los números de canal lógico del 1 al 16. Estos números de canal lógico corresponden a los números de canal físicos del 0 al 15 que realmente forman parte del mensaje DE MIDI. Todas las referencias a los valores de clave y cambio de programa de MIDI usan los valores físicos del 0 al 127. Todos los números son decimales a menos que estén precedidos del prefijo "0x", en cuyo caso son hexadecimales.

En la explicación del asignador de MIDI, el término *origen* hace referencia al lado de entrada del asignador DE MIDI. El término *destino hace* referencia al lado de salida del asignador de MIDI. Por ejemplo, un canal de origen es el canal MIDI de un mensaje enviado al asignador de MIDI y un canal de destino es el canal MIDI de un mensaje enviado desde el Asignador DE MIDI a un dispositivo de salida.

-   [El asignador y el Windows](the-midi-mapper-and-windows.md)
-   [Arquitectura del asignador de MIDI](the-midi-mapper-architecture.md)
-   [Mapa de canal](the-channel-map.md)
-   [Aplicación de Mapas](patch-maps.md)
-   [Escalar de volumen](the-volume-scalar.md)
-   [Clave Mapas](key-maps.md)
-   [Resumen de mensajes Mapas y MIDI](summary-of-maps-and-midi-messages.md)

 

 




