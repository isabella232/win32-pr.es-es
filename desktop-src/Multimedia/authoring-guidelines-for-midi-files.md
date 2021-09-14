---
title: Directrices de creación para archivos MIDI
description: Directrices de creación para archivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Interfaz digital de instrumentación de música (MIDI), directrices de creación de archivos
- MIDI (Interfaz digital de instrumentación de música), directrices de creación de archivos
- crear archivos MIDI, directrices de creación de archivos
- asignaciones de revisiones ESTÁNDAR DE MIDI
- asignaciones de claves MIDI estándar
- Interfaz digital instrumentable (MIDI), asignaciones de revisiones estándar
- MIDI (Interfaz digital instrumentable), asignaciones de revisiones estándar
- Interfaz digital de instrumentar música (MIDI), asignaciones de claves estándar
- MIDI (Interfaz digital instrumentable), asignaciones de claves estándar
- crear archivos MIDI, asignaciones de revisiones estándar
- crear archivos MIDI, asignaciones de claves estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062966"
---
# <a name="authoring-guidelines-for-midi-files"></a>Directrices de creación para archivos MIDI

Siga estas instrucciones para crear archivos MIDI independientes del dispositivo para Windows:

-   Use las [asignaciones de revisión estándar](standard-midi-patch-assignments.md) de MIDI y [las asignaciones de claves MIDI estándar.](standard-midi-key-assignments.md)
-   Envíe siempre un mensaje de cambio de programa a un canal para seleccionar una revisión antes de enviar otros mensajes a ese canal. Para los dos canales de televisión (10 y 16), seleccione el número de programa 0.
-   Siga siempre un mensaje de cambio de programa DE MIDI con un mensaje de controlador de volumen principal DE MIDI (número de controlador 7) para establecer el volumen relativo de la revisión.
-   Use un valor de 80 (0x50) para el controlador de volumen principal para los niveles de escucha normales. Para niveles más silenciosos o más altos, puede usar valores inferiores o superiores.
-   Use solo los siguientes mensajes MIDI: note-on with velocity, note-off, program change, pitch pitch pitch, main volume (controller 7) y el controlador 64. Los síntesis internos son necesarios para responder a estos mensajes y la mayoría de los instrumentos son tan importantes como para responder a ellos.

 

 




