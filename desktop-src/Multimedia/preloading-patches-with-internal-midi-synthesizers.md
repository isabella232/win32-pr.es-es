---
title: Carga previa de revisiones con sintetizadores MIDI internos
description: Carga previa de revisiones con sintetizadores MIDI internos
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Interfaz digital de instrumentos musicales (MIDI), sintetizadores internos
- MIDI (interfaz digital de instrumentos musicales), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- Sintetizadores MIDI internos
- Interfaz digital de instrumentos musicales (MIDI), precarga de revisiones
- MIDI (interfaz digital de instrumentos musicales), precarga de revisiones
- reproducir archivos MIDI, carga previa de revisiones
- carga previa de revisiones MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995165"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Carga previa de revisiones con sintetizadores MIDI internos

Algunos dispositivos de sintetizador MIDI internos no pueden mantener todas las revisiones cargadas simultáneamente. Estos dispositivos deben cargar previamente los datos de revisión.

Windows proporciona las siguientes funciones para solicitar que un sintetizador precargue y almacene en caché las revisiones especificadas.



| Value                                                      | Significado                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Solicita que un dispositivo de sintetizador MIDI interno precargue y almacene en caché las revisiones de melodic especificadas.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Solicita que un dispositivo de sintetizador MIDI interno precargue y almacene en caché las revisiones de percusión basadas en clave especificadas. |



 

Para obtener información sobre cómo determinar si un dispositivo determinado admite revisiones de carga previa, consulte [consultar los dispositivos de salida MIDI](querying-midi-output-devices.md).

 

 