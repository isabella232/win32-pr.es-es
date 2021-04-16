---
title: Consulta de dispositivos de salida MIDI
description: Consulta de dispositivos de salida MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida MIDI
- Interfaz digital de instrumentos musicales (MIDI), consultando dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), consultar los dispositivos de salida
- reproducir archivos MIDI, consultar los dispositivos de salida
- consulta de dispositivos de salida MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676363"
---
# <a name="querying-midi-output-devices"></a>Consulta de dispositivos de salida MIDI

Antes de reproducir un archivo MIDI, debe usar la función [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) para determinar las capacidades del dispositivo de salida MIDI que está presente en el sistema. Esta función toma una dirección de una estructura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) , que rellena con información sobre las capacidades del dispositivo especificado. Esta información incluye los identificadores de fabricante y de producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo (especificado en los miembros **wMid**, **wPid**, **szPname** y **vDriverVersion** , respectivamente).

Los dispositivos de salida MIDI pueden ser sintetizadores internos o puertos de salida MIDI externos. El miembro **wTechnology** de la estructura **MIDIOUTCAPS** especifica la tecnología del dispositivo.

Si el dispositivo es un sintetizador interno, la información adicional del dispositivo está disponible en los miembros **wVoices**, **wNotes** y **wChannelMask** . El miembro **wVoices** especifica el número de voces que admite el dispositivo. Cada voz puede tener un sonido o timbre diferentes. Las voces están organizadas en canales MIDI. El miembro **wNotes** *especifica la polisonante* del dispositivo, es decir, el número máximo de notas que se pueden reproducir simultáneamente. El miembro **wChannelMask** es una representación de bits de los canales MIDI a los que responde el dispositivo. Por ejemplo, si el dispositivo responde a los ocho primeros canales MIDI, **wChannelMask** es 0x00FF. Si el dispositivo es un puerto de salida externo, **wVoices** y **wNotes** no se usan y **wChannelMask** se establece en 0xFFFF.

El miembro **dwSupport** de la estructura **MIDIOUTCAPS** indica si el controlador de dispositivo admite cambios de volumen, almacenamiento en caché de revisiones y transmisión por secuencias. Solo los dispositivos de sintetizador internos admiten los cambios de volumen. Los puertos de salida MIDI externos no admiten cambios de volumen. Para obtener información sobre cómo cambiar el volumen, consulte [cambiar el volumen del sintetizador MIDI interno](changing-internal-midi-synthesizer-volume.md).

 

 