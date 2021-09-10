---
title: Consulta de dispositivos de entrada DE LÍNEA
description: Consulta de dispositivos de entrada DE LÍNEA
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Interfaz digital instrumentable (MIDI), dispositivos de entrada
- MIDI (Interfaz digital de instrumentar música), dispositivos de entrada
- grabación de audio MIDI, dispositivos de entrada
- Dispositivos de entrada DE LÍNEA
- Interfaz digital de instrumentación de música (MIDI), consulta de dispositivos de entrada
- MIDI (Interfaz digital de instrumentación instrumental), consulta de dispositivos de entrada
- grabación de audio MIDI, consulta de dispositivos de entrada
- consulta de dispositivos de entrada DE LÍNEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370915"
---
# <a name="querying-midi-input-devices"></a>Consulta de dispositivos de entrada DE LÍNEA

Antes de grabar audio MIDI, debe usar la función [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) para determinar las funcionalidades del dispositivo de entrada MIDI que está presente en el sistema. Esta función toma una dirección de una estructura [**MIDIINCAPS,**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) que rellena con información sobre las funcionalidades del dispositivo determinado. Esta información incluye el fabricante y los identificadores de producto, un nombre de producto para el dispositivo y el número de versión del controlador del dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 