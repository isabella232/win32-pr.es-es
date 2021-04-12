---
title: Arquitectura del asignador MIDI
description: Arquitectura del asignador MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignador MIDI
- MIDI (interfaz digital de instrumentos musicales), asignador MIDI
- Asignador de MIDI, arquitectura
- Asignador de MIDI, mapa de configuración
- Mapa de configuración de MIDI
- Asignador de MIDI, mapa de canales
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas de claves
- mapa de canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357495"
---
# <a name="the-midi-mapper-architecture"></a>Arquitectura del asignador MIDI

El asignador MIDI utiliza un mapa de configuración de MIDI para determinar cómo trasladar y redirigir los mensajes que recibe. Un mapa de configuración de MIDI consta de los siguientes tipos de mapas.

-   [Asignación de canal](the-channel-map.md)
-   [Mapas de revisiones](patch-maps.md)
-   [Mapas de claves](key-maps.md)

En la ilustración siguiente se muestran los roles de canal, revisión y mapas de claves en un mapa de configuración de MIDI.

![los roles de canal, revisión y mapas de claves en una imagen de mapa de configuración de MIDI](images/mmap-a02.gif)

 

 




