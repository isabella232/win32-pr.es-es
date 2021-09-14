---
title: Arquitectura del asignador de MIDI
description: Arquitectura del asignador de MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
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
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260719"
---
# <a name="the-midi-mapper-architecture"></a>Arquitectura del asignador de MIDI

El Asignador de MIDI usa un mapa de configuración de MIDI para determinar cómo traducir y redirigir los mensajes que recibe. Un mapa de configuración de MIDI consta de los siguientes tipos de mapas.

-   [Mapa de canal](the-channel-map.md)
-   [Aplicación de Mapas](patch-maps.md)
-   [Clave Mapas](key-maps.md)

En la ilustración siguiente se muestran los roles de los mapas de canal, revisión y clave en un mapa de configuración de MIDI.

![los roles de mapas de canal, revisión y clave en una imagen de mapa de configuración de midi](images/mmap-a02.gif)

 

 




