---
title: Precarga de revisiones con síntesis INTERNA DE MIDI
description: Precarga de revisiones con síntesis INTERNA DE MIDI
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Interfaz digital instrumentable (MIDI), sintetizadores internos
- MIDI (Interfaz digital de instrumentado), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- sintetizadores INTERNOS DE MIDI
- Interfaz digital de instrumentación de música (MIDI), precarga de revisiones
- MIDI (Interfaz digital de instrumentación de música), precarga de revisiones
- reproducir archivos MIDI, cargar previamente revisiones
- precarga de revisiones de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372502"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Precarga de revisiones con síntesis INTERNA DE MIDI

Algunos dispositivos de síntesis MIDI internos no pueden mantener todas sus revisiones cargadas simultáneamente. Estos dispositivos deben cargar previamente sus datos de revisión.

Windows proporciona las siguientes funciones para solicitar que un sintetizador precargue y en caché las revisiones especificadas.



| Valor                                                      | Significado                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Solicita que un dispositivo de síntesis MIDI interno precargue y en caché las revisiones melodicas especificadas.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Solicita que un dispositivo de síntesis MIDI interno precargue y en caché las revisiones de revisión de revisión basadas en claves especificadas. |



 

Para obtener información sobre cómo determinar si un dispositivo determinado admite la carga previa de revisiones, vea [Consulta de dispositivos de salida DE MIDI.](querying-midi-output-devices.md)

 

 