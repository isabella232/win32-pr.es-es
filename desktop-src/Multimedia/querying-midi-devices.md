---
title: Consulta de dispositivos MIDI
description: Consulta de dispositivos MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Interfaz digital de instrumentación de música (MIDI), consultar dispositivos
- MIDI (Interfaz digital de instrumentación de música), consulta de dispositivos
- Servicios DE MIDI, consultar dispositivos
- consultar dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171578"
---
# <a name="querying-midi-devices"></a>Consulta de dispositivos MIDI

Antes de reproducir o grabar datos DE MIDI, debe determinar las capacidades del hardware de MIDI presente en el sistema. La funcionalidad de MIDI puede variar de un equipo multimedia al siguiente; las aplicaciones no deben hacer suposiciones sobre el hardware presente en un sistema determinado.

Windows proporciona las siguientes funciones para determinar cuántos dispositivos MIDI están disponibles para la entrada o salida en un sistema determinado.



| Value                                          | Significado                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Recupera el número de dispositivos de entrada de MIDI presentes en el sistema.  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Recupera el número de dispositivos de salida DE MIDI presentes en el sistema. |



 

Al igual que otros dispositivos de audio, los dispositivos MIDI se identifican mediante un identificador de dispositivo, que se determina implícitamente a partir del número de dispositivos presentes en un sistema determinado. Los identificadores de dispositivo oscilan entre cero y el número de dispositivos presentes, menos uno. Por ejemplo, si hay dos dispositivos de salida MIDI en un sistema, los identificadores de dispositivo válidos son 0 y 1.

Después de determinar cuántos dispositivos de entrada o salida DE LÍNEA están presentes en un sistema, puede consultar las funcionalidades de cada dispositivo. Windows proporciona las siguientes funciones para determinar las funcionalidades de los dispositivos de audio.



| Value                                          | Significado                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Recupera las funcionalidades de un dispositivo de entrada MIDI determinado y coloca esta información en la [**estructura MIDIINCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Recupera las funcionalidades de un dispositivo de salida MIDI determinado y coloca esta información en la [**estructura MIDIOUTCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) |



 

Cada una de estas funciones tiene un parámetro que especifica la dirección de una estructura que la función rellena con información sobre las funcionalidades de un dispositivo especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 