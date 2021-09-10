---
title: Crear archivos MIDI
description: Crear archivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimedia, crear archivos MIDI
- multimedia, crear archivos MIDI
- audio multimedia, creación de archivos MIDI
- audio, crear archivos MIDI
- Interfaz digital de instrumentar música (MIDI), crear archivos
- MIDI (Interfaz digital instrumenta de música), creación de archivos
- crear archivos MIDI, acerca de
- Asociación de fabricantes de MIDI (MMA)
- MMA (Asociación de fabricantes de MIDI)
- Especificación detallada de MIDI
- Especificación estándar de archivos MIDI
- Especificación general de MIDI (GM)
- Especificación de GM (GENERAL MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370801"
---
# <a name="creating-midi-files"></a>Crear archivos MIDI

Las especificaciones de la interfaz digital de instrumentación cultural (MIDI) están publicadas por y son materiales protegidos por derechos de autor de la Asociación de fabricantes de MIDI (MMA). En la lista siguiente se describen las especificaciones que son de mayor interés general:

## <a name="midi-detailed-specification"></a>Especificación detallada de MIDI

La especificación detallada de MIDI explica los protocolos de hardware y software de MIDI. Esto es útil para aquellos que desarrollan aplicaciones multimedia que implementan compatibilidad con MIDI mediante el uso de funciones DE MIDI para grabar, editar o reproducir datos DE MIDI.

## <a name="standard-midi-files-10"></a>Standard MIDI Files 1.0

La especificación Standard MIDI Files define una manera de intercambiar datos DE MIDI con marca de tiempo entre distintas aplicaciones en la misma plataforma de hardware o en distintas. Esto resulta útil para los desarrolladores que escriben aplicaciones que leen y analizan archivos de disco que contienen datos DE MIDI o que escriben archivos de datos DE MIDI en el disco.

## <a name="general-midi-system---level-1"></a>Sistema GENERAL DE MIDI: nivel 1

La especificación GENERAL DE MIDI (GM) define una configuración mínima de MIDI de un "Sistema GENERAL DE MIDI". Este sistema consta de una clase específica de dispositivos de reproducción de MIDI y es de interés para los desarrolladores multimedia que han creado archivos MIDI. La mayoría de las tarjetas de sonido de PC y los sintetizadores MIDI fabricados hoy en día son compatibles con la especificación de GM. Por lo general, los archivos MIDI creados para la especificación de GM deberían parecer como estaban diseñados para sonar, independientemente del dispositivo compatible con GM en el que se reproducen.

Para permitir que los archivos MIDI sean un formato viable para representar música en la informática multimedia, Windows sigue la especificación general del nivel 1 del sistema MIDI. En los temas siguientes se proporcionan directrices de creación de MIDI adicionales:

-   [Directrices de creación para archivos MIDI](authoring-guidelines-for-midi-files.md)
-   [Asignaciones de revisiones ESTÁNDAR DE MIDI](standard-midi-patch-assignments.md)
-   [Asignaciones de claves MIDI estándar](standard-midi-key-assignments.md)

 

 




