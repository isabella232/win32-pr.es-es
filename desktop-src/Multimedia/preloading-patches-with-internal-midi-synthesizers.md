---
title: Precarga de revisiones con sintetizadores internos de MIDI
description: Precarga de revisiones con sintetizadores internos de MIDI
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Interfaz digital de instrumentar música (MIDI), sintetizadores internos
- MIDI (Interfaz digital de instrumentado), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- sintetizadores internos de MIDI
- Interfaz digital de instrumentación musical (MIDI), precarga de revisiones
- MIDI (Interfaz digital de instrumentación de música), precarga de revisiones
- reproducir archivos MIDI, cargar previamente revisiones
- precarga de revisiones de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371000"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Precarga de revisiones con sintetizadores internos de MIDI

Algunos dispositivos de síntesis INTERNA de MIDI no pueden mantener todas sus revisiones cargadas simultáneamente. Estos dispositivos deben cargar previamente sus datos de revisión.

Windows proporciona las siguientes funciones para solicitar que un sintetizador precargue y en caché las revisiones especificadas.



| Value                                                      | Significado                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Solicita que un dispositivo de síntesis MIDI interno precargue y en caché las revisiones meódicas especificadas.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Solicita que un dispositivo de síntesis MIDI interno precargue y en caché las revisiones de revisión de revisión basadas en claves especificadas. |



 

Para obtener información sobre cómo determinar si un dispositivo determinado admite la carga previa de revisiones, vea [Consulta de dispositivos de salida DE MIDI.](querying-midi-output-devices.md)

 

 