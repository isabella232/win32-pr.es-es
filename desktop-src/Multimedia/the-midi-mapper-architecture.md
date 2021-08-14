---
title: Arquitectura del asignador de MIDI
description: Arquitectura del asignador de MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Interfaz digital de instrumentar música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital instrumenta instrumenta),Asignador DE MIDI
- Asignador de MIDI, arquitectura
- Asignador de MIDI, mapa de configuración
- Mapa de configuración de MIDI
- Asignador de MIDI, mapa de canal
- Asignador de MIDI, mapas de revisiones
- Asignador de MIDI, mapas de claves
- channel map
- mapas de revisión
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a20e73c9a361487468870698d3c36d59ef35bb6a28da1b03957dd24f1d7b7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136412"
---
# <a name="the-midi-mapper-architecture"></a>Arquitectura del asignador de MIDI

El Asignador de MIDI usa un mapa de configuración de MIDI para determinar cómo traducir y redirigir los mensajes que recibe. Un mapa de configuración de MIDI consta de los siguientes tipos de mapas.

-   [Mapa de canal](the-channel-map.md)
-   [Aplicación de Mapas](patch-maps.md)
-   [Clave Mapas](key-maps.md)

En la ilustración siguiente se muestran los roles de los mapas de canal, revisión y clave en un mapa de configuración de MIDI.

![los roles de mapas de canal, revisión y clave en una imagen de mapa de configuración de midi](images/mmap-a02.gif)

 

 




