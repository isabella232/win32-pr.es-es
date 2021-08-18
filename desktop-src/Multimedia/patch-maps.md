---
title: Aplicación de Mapas
description: Aplicación de Mapas
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música), Asignador de MIDI
- Asignador de MIDI, mapas de revisiones
- mapas de revisión
- Mensajes de cambio de programa DE MIDI
- Mensajes del controlador de volumen DE MIDI
- mensajes de cambio de programa
- mensajes de controlador de volumen
- Asignador de MIDI, mensajes de cambio de programa
- Asignador de MIDI, mensajes de controlador de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32f60ac486d7e8812b5cf71febe3794ae37d650bc795baa4c06ffb48ce5f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038274"
---
# <a name="patch-maps"></a>Aplicación de Mapas

Cada entrada del mapa de canal puede tener un mapa de revisión asociado. Los mapas de revisiones afectan a los mensajes de cambio de programa y controlador de volumen de MIDI. Los mensajes de cambio de programa le piden a un sintetizador que cambie el sonido del instrumento (revisión) de un canal especificado. Los mensajes del controlador de volumen establecen el volumen de un canal.

Un mapa de revisiones tiene una tabla de traducción con una entrada para cada uno de los 128 valores de cambio de programa. Cada mapa de revisión especifica lo siguiente:

-   Valor de cambio de programa de destino.
-   Un volumen escalar. (Para obtener más información, vea [El volumen escalar).](the-volume-scalar.md)
-   Un mapa de claves opcional. (Para obtener más información, vea [Key Mapas](key-maps.md)).

Cuando el asignador de MIDI recibe mensajes de cambio de programa, el valor de cambio del programa de destino se sustituye por el valor de cambio de programa en el mensaje. Por ejemplo, si el valor de program-change de destino para program-change 16 es 18, el asignador de MIDI modifica el mensaje de cambio de programa DE MIDI como se muestra en la ilustración siguiente.

![imagen del asignador de midi](images/mmap-a03.gif)

 

 




