---
title: Aplicación de Mapas
description: Aplicación de Mapas
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, mapas de revisiones
- mapas de revisiones
- Mensajes de cambio de programa de MIDI
- Mensajes de controlador de volumen DE MIDI
- mensajes de cambio de programa
- mensajes de controlador de volumen
- Asignador de MIDI, mensajes de cambio de programa
- Asignador de MIDI, mensajes de controlador de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161398"
---
# <a name="patch-maps"></a>Aplicación de Mapas

Cada entrada del mapa de canal puede tener un mapa de revisión asociado. Los mapas de revisiones afectan a los mensajes de cambio de programa y de controlador de volumen de MIDI. Los mensajes de cambio de programa le piden a un sintetizador que cambie el sonido de instrumentar (revisión) de un canal especificado. Los mensajes del controlador de volumen establecen el volumen de un canal.

Un mapa de revisiones tiene una tabla de traducción con una entrada para cada uno de los 128 valores de cambio de programa. Cada mapa de revisiones especifica lo siguiente:

-   Valor de cambio del programa de destino.
-   Un volumen escalar. (Para obtener más información, [vea El volumen escalar).](the-volume-scalar.md)
-   Un mapa de claves opcional. (Para obtener más información, vea [Key Mapas](key-maps.md)).

Cuando el asignador de MIDI recibe mensajes de cambio de programa, el valor de cambio del programa de destino se sustituye por el valor de cambio de programa en el mensaje. Por ejemplo, si el valor de program-change de destino para program-change 16 es 18, el asignador de MIDI modifica el mensaje de cambio de programa DE MIDI como se muestra en la ilustración siguiente.

![imagen de mapeador de midi](images/mmap-a03.gif)

 

 




