---
title: Cambiar el volumen interno del síntesis DE MIDI
description: Cambiar el volumen interno del síntesis DE MIDI
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Interfaz digital instrumentable (MIDI), sintetizadores internos
- MIDI (Interfaz digital de instrumentado), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- sintetizadores INTERNOS DE MIDI
- Interfaz digital instrumentable (MIDI), cambio de volumen
- MIDI (Interfaz digital de instrumentado), cambio de volumen
- reproducir archivos MIDI, cambiar volumen
- cambiar el volumen de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c7e17a7e8c0a6902e26dd8bbfdf8eb89c39297fdacdf062749d8c47a3d487
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808215"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Cambiar el volumen interno del síntesis DE MIDI

Windows proporciona las siguientes funciones para recuperar y establecer el nivel de volumen de los dispositivos de síntesis DE MIDI internos:



| Valor                                        | Significado                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera el nivel de volumen del dispositivo de síntesis MIDI interno especificado. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Establece el nivel de volumen del dispositivo de síntesis MIDI interno especificado.      |



 

No todos los dispositivos de salida DE MIDI admiten cambios de volumen. Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho. Para obtener información sobre cómo determinar si un dispositivo determinado admite cambios de volumen, vea [Consulta de dispositivos de salida DE MIDI.](querying-midi-output-devices.md)

A menos que la aplicación esté diseñada para ser una aplicación maestra de control de volumen (proporciona al usuario control de volumen para todos los dispositivos de audio de un sistema), debe abrir un dispositivo de audio antes de cambiar su volumen. También debe comprobar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.

El volumen se especifica como un valor doubleword. Los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.

En el caso de los dispositivos que no admiten cambios de volumen individuales en los canales izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y los 16 bits superiores se omiten. Los valores del nivel de volumen van 0x0 (silencio) a 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento del volumen percibido es el mismo al aumentar el nivel de volumen de 0x5000 a 0x6000, ya que va de 0x4000 a 0x5000.

 

 