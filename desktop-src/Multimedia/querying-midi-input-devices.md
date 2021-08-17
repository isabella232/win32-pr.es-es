---
title: Consulta de dispositivos de entrada DE LÍNEA
description: Consulta de dispositivos de entrada DE LÍNEA
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Interfaz digital instrumentable (MIDI), dispositivos de entrada
- MIDI (Interfaz digital de instrumentar música), dispositivos de entrada
- grabación de audio MIDI, dispositivos de entrada
- Dispositivos de entrada DE LÍNEA
- Interfaz digital instrumentable (MIDI), consulta de dispositivos de entrada
- MIDI (Interfaz digital de instrumentación instrumental), consulta de dispositivos de entrada
- grabación de audio MIDI, consulta de dispositivos de entrada
- consulta de dispositivos de entrada DE LÍNEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371937"
---
# <a name="querying-midi-input-devices"></a>Consulta de dispositivos de entrada DE LÍNEA

Antes de grabar audio MIDI, debe usar la función [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) para determinar las funcionalidades del dispositivo de entrada MIDI que está presente en el sistema. Esta función toma una dirección de una estructura [**MIDIINCAPS,**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) que rellena con información sobre las funcionalidades del dispositivo determinado. Esta información incluye los identificadores de fabricante y producto, un nombre de producto para el dispositivo y el número de versión del controlador del dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 