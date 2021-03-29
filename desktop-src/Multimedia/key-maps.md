---
title: Mapas de claves
description: Mapas de claves
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, mapas de claves
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994079"
---
# <a name="key-maps"></a>Mapas de claves

Cada entrada de la tabla de traducción patch-Map puede tener asociado un mapa de claves. Los mapas de claves afectan a los mensajes de Nota: on, note-off y Polyphonic-Key-aftertouch. Un mapa de claves tiene una tabla de traducción con una entrada para cada uno de los valores de clave MIDI 128. Por ejemplo, si la entrada del valor de clave 60 es 72, el asignador de MIDI modifica los mensajes de la nota de MIDI, tal y como se muestra en la siguiente ilustración.

![imagen del asignador MIDI](images/mmap-a06.gif)

Los mapas de claves son útiles con los sintetizadores que tienen instrumentos de percusión basados en claves con un sonido de percusión determinado asignado a cada clave. Normalmente, los mapas de claves se asignan a la primera revisión de las asignaciones de revisión en los canales de percusión (10 y 16).

 

 




