---
title: Consulta de dispositivos de salida de MIDI
description: Consulta de dispositivos de salida de MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Interfaz digital de instrumentar música (MIDI), dispositivos de salida
- MIDI (Interfaz digital de instrumentar música), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida DE MIDI
- Interfaz digital de instrumentación musical (MIDI), consulta de dispositivos de salida
- MIDI (Interfaz digital de instrumentación de música), consultar dispositivos de salida
- reproducir archivos MIDI, consultar dispositivos de salida
- consulta de dispositivos de salida de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b493c0b3554a9a60cfc349d13a5404ec4d2b27915933c14b387df29a582406e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371917"
---
# <a name="querying-midi-output-devices"></a>Consulta de dispositivos de salida de MIDI

Antes de reproducir un archivo MIDI, debe usar la función [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) para determinar las funcionalidades del dispositivo de salida MIDI que está presente en el sistema. Esta función toma una dirección de una [**estructura MIDIOUTCAPS,**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) que rellena con información sobre las funcionalidades del dispositivo determinado. Esta información incluye los identificadores de fabricante y producto, un nombre de producto para el dispositivo y el número de versión del controlador del dispositivo (especificado en los miembros **wMid**, **wPid**, **szPname** y **vDriverVersion,** respectivamente).

Los dispositivos de salida DE MIDI pueden ser sintetizadores internos o puertos de salida EXTERNOS DE MIDI. El **miembro wTechnology** de la **estructura MIDIOUTCAPS** especifica la tecnología del dispositivo.

Si el dispositivo es un sintetizador interno, hay información adicional sobre el dispositivo disponible en los miembros **wVoices**, **wNotes** y **wChannelMask.** El **miembro wVoices** especifica el número de voces que admite el dispositivo. Cada voz puede tener un sonido o timbre diferentes. Las voces se organizan en canales MIDI. El **miembro wNotes** especifica la *polifónica* del dispositivo, es decir, el número máximo de notas que se pueden reproducir simultáneamente. El **miembro wChannelMask** es una representación de bits de los canales MIDI a los que responde el dispositivo. Por ejemplo, si el dispositivo responde a los ocho primeros canales DE MIDI, **wChannelMask** se 0x00FF. Si el dispositivo es un puerto de salida externo, **wVoices** y **wNotes** no se usan y **wChannelMask** se establece en 0xFFFF.

El **miembro dwSupport** de la **estructura MIDIOUTCAPS** indica si el controlador de dispositivo admite cambios de volumen, almacenamiento en caché de revisiones y streaming. Los cambios de volumen solo son compatibles con dispositivos de síntesis internos. Los puertos de salida EXTERNOs de MIDI no admiten cambios de volumen. Para obtener información sobre cómo cambiar el volumen, vea [Changing Internal MIDI Synthesizer Volume](changing-internal-midi-synthesizer-volume.md).

 

 