---
title: Instrucciones de creación para archivos MIDI
description: Instrucciones de creación para archivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), instrucciones para la creación de archivos
- MIDI (interfaz digital de instrumentos musicales), instrucciones para la creación de archivos
- creación de archivos MIDI, instrucciones para la creación de archivos
- asignaciones estándar de revisión MIDI
- asignaciones de claves MIDI estándar
- Interfaz digital de instrumentos musicales (MIDI), asignaciones de revisiones estándar
- MIDI (interfaz digital de instrumentos musicales), asignaciones de revisiones estándar
- Interfaz digital de instrumentos musicales (MIDI), asignaciones de claves estándar
- MIDI (interfaz digital de instrumentos musicales), asignaciones de clave estándar
- creación de archivos MIDI, asignaciones de revisiones estándar
- crear archivos MIDI, asignaciones de clave estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076279"
---
# <a name="authoring-guidelines-for-midi-files"></a>Instrucciones de creación para archivos MIDI

Siga estas instrucciones para crear archivos MIDI independientes del dispositivo para Windows:

-   Use las [asignaciones estándar de revisión de MIDI](standard-midi-patch-assignments.md) y las [asignaciones de clave MIDI estándar](standard-midi-key-assignments.md).
-   Envíe siempre un mensaje de cambio de programa a un canal para seleccionar una revisión antes de enviar otros mensajes a ese canal. Para los dos canales de percusión (10 y 16), seleccione el número de programa 0.
-   Siga siempre un mensaje de cambio de programa MIDI con un mensaje de controlador de volumen principal MIDI (número de controlador 7) para establecer el volumen relativo de la revisión.
-   Use un valor de 80 (0x50) para el controlador de volumen principal para los niveles de escucha normales. Para niveles más silenciosos o más altos, puede usar valores inferiores o superiores.
-   Use solo los siguientes mensajes MIDI: tenga en cuenta la velocidad, el cambio de la nota, la desactivación, el cambio de programa, el plegado de paso, el volumen principal (controlador 7) y el pedal del amortiguador (controlador 64). Los sintetizadores internos son necesarios para responder a estos mensajes y la mayoría de los instrumentos musicales MIDI también responden a ellos.

 

 




