---
title: Mapas de revisiones
description: Mapas de revisiones
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapas de revisiones
- mapas de revisiones
- 'Programa MIDI: mensajes de cambio'
- Mensajes de controlador de volumen MIDI
- mensajes de cambio de programa
- mensajes de controlador de volumen
- Asignador de MIDI, mensajes de cambio de programa
- Asignador de MIDI, mensajes de controlador de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357008"
---
# <a name="patch-maps"></a>Mapas de revisiones

Cada entrada de mapa de canal puede tener una asignación de revisión asociada. Las asignaciones de revisiones afectan a los mensajes de cambio de programa MIDI y de controlador de volumen. Los mensajes de cambio de programa indican a un sintetizador que cambie el sonido del instrumento (revisión) de un canal especificado. Los mensajes de Volume Controller establecen el volumen de un canal.

Una asignación de revisión tiene una tabla de traducción con una entrada para cada uno de los valores de cambio de programa de 128. Cada asignación de revisión especifica lo siguiente:

-   Valor de cambio de programa de destino.
-   Escalar del volumen. (Para obtener más información, vea [el volumen escalar](the-volume-scalar.md)).
-   Un mapa de claves opcional. (Para obtener más información, consulte [mapas de claves](key-maps.md)).

Cuando el asignador MIDI recibe los mensajes de cambio de programa, el valor de cambio de programa de destino se sustituye por el valor de cambio de programa en el mensaje. Por ejemplo, si el programa de destino-Change Value for Program-Change 16 es 18, el asignador MIDI modifica el mensaje de cambio de programa MIDI tal y como se muestra en la siguiente ilustración.

![imagen del asignador MIDI](images/mmap-a03.gif)

 

 




