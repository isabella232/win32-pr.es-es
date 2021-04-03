---
title: Crear archivos MIDI
description: Crear archivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimedia, crear archivos MIDI
- multimedia, crear archivos MIDI
- audio multimedia, crear archivos MIDI
- audio, creación de archivos MIDI
- Interfaz digital de instrumentos musicales (MIDI), crear archivos
- MIDI (interfaz digital de instrumentos musicales), crear archivos
- crear archivos MIDI, acerca de
- Asociación de fabricantes de MIDI (MMA)
- MMA (Asociación de fabricantes de MIDI)
- Especificación detallada de MIDI
- Especificación de archivos MIDI estándar
- Especificación MIDI general (GM)
- Especificación GM (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075442"
---
# <a name="creating-midi-files"></a>Crear archivos MIDI

Las especificaciones de la interfaz digital de instrumentos musicales (MIDI) están publicadas por y son material protegido por derechos de autor de la Asociación de fabricantes de MIDI (MMA). En la lista siguiente se describen las especificaciones de mayor interés general:

## <a name="midi-detailed-specification"></a>Especificación detallada de MIDI

La especificación detallada de MIDI explica los protocolos de hardware y software de MIDI. Esto resulta útil para aquellos que desarrollan aplicaciones multimedia que implementan la compatibilidad con MIDI mediante el uso de funciones MIDI para grabar, editar o reproducir datos MIDI.

## <a name="standard-midi-files-10"></a>Archivos MIDI estándar 1,0

La especificación de archivos MIDI estándar define una manera de intercambiar datos MIDI con marca de tiempo entre diferentes aplicaciones en la misma plataforma de hardware o en distintas plataformas. Esto resulta útil para los programadores que escriben aplicaciones que leen y analizan archivos de disco que contienen datos MIDI o escriben archivos de datos MIDI en el disco.

## <a name="general-midi-system---level-1"></a>Nivel de sistema MIDI general 1

La especificación MIDI general (GM) define una configuración de MIDI mínima de un "sistema MIDI general". Este sistema se compone de una clase específica de dispositivos de reproducción MIDI y es de interés para los desarrolladores multimedia que crean archivos MIDI. La mayoría de las tarjetas de sonido de PC y los sintetizadores MIDI fabricados hoy en día son compatibles con la especificación GM. Por lo general, los archivos MIDI que se crean con la especificación GM deben sonar tal y como están destinados a sonar, independientemente del dispositivo compatible con GM en el que se reproduzcan.

Para permitir que los archivos MIDI tengan un formato viable para representar música en la informática multimedia, Windows sigue la especificación general de nivel 1 del sistema MIDI. En los temas siguientes se proporcionan instrucciones adicionales para la creación de MIDI:

-   [Instrucciones de creación para archivos MIDI](authoring-guidelines-for-midi-files.md)
-   [Asignaciones estándar de revisión MIDI](standard-midi-patch-assignments.md)
-   [Asignaciones de claves MIDI estándar](standard-midi-key-assignments.md)

 

 




