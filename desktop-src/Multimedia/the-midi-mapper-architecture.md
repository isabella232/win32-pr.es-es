---
title: Arquitectura del asignador de MIDI
description: Arquitectura del asignador de MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, arquitectura
- Asignador de MIDI, mapa de configuración
- Mapa de configuración de MIDI
- Asignador de MIDI, mapa de canal
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas clave
- mapa del canal
- mapas de revisiones
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371072"
---
# <a name="the-midi-mapper-architecture"></a>Arquitectura del asignador de MIDI

El asignador de MIDI usa un mapa de configuración de MIDI para determinar cómo traducir y redirigir los mensajes que recibe. Un mapa de configuración de MIDI consta de los siguientes tipos de mapas.

-   [Mapa del canal](the-channel-map.md)
-   [Aplicación de Mapas](patch-maps.md)
-   [Clave Mapas](key-maps.md)

En la ilustración siguiente se muestran los roles de los mapas de canal, revisión y clave en un mapa de configuración de MIDI.

![los roles de mapas de canal, revisión y clave en una imagen de mapa de configuración de Midi](images/mmap-a02.gif)

 

 




