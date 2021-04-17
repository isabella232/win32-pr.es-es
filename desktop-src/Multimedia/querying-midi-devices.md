---
title: Consulta de dispositivos MIDI
description: Consulta de dispositivos MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Interfaz digital de instrumentos musicales (MIDI), consultar dispositivos
- MIDI (interfaz digital de instrumentos musicales), consultar dispositivos
- Servicios MIDI, consultar dispositivos
- consulta de dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420580"
---
# <a name="querying-midi-devices"></a>Consulta de dispositivos MIDI

Antes de reproducir o grabar datos MIDI, debe determinar las capacidades del hardware de MIDI presente en el sistema. La capacidad MIDI puede variar de un equipo multimedia a otro; las aplicaciones no deben hacer suposiciones sobre el hardware presente en un sistema determinado.

Windows proporciona las siguientes funciones para determinar el número de dispositivos MIDI que están disponibles para la entrada o la salida en un sistema determinado.



| Value                                          | Significado                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Recupera el número de dispositivos de entrada MIDI presentes en el sistema.  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Recupera el número de dispositivos de salida MIDI presentes en el sistema. |



 

Al igual que otros dispositivos de audio, los dispositivos MIDI se identifican mediante un identificador de dispositivo, que se determina implícitamente a partir del número de dispositivos presentes en un sistema determinado. Los identificadores de dispositivo van desde cero hasta el número de dispositivos presentes, menos uno. Por ejemplo, si hay dos dispositivos de salida MIDI en un sistema, los identificadores de dispositivo válidos son 0 y 1.

Después de determinar el número de dispositivos de entrada o salida MIDI presentes en un sistema, puede consultar las capacidades de cada dispositivo. Windows proporciona las siguientes funciones para determinar las capacidades de los dispositivos de audio.



| Value                                          | Significado                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Recupera las capacidades de un dispositivo de entrada MIDI determinado y coloca esta información en la estructura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Recupera las capacidades de un dispositivo de salida MIDI determinado y coloca esta información en la estructura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) . |



 

Cada una de estas funciones tiene un parámetro que especifica la dirección de una estructura que la función rellena con información sobre las capacidades de un dispositivo especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 