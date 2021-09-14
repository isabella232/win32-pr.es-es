---
title: Cambiar el volumen interno del sintetizador de MIDI
description: Cambiar el volumen interno del sintetizador de MIDI
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Interfaz digital de instrumentar música (MIDI), sintetizadores internos
- MIDI (Interfaz digital de instrumentado), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- sintetizadores internos de MIDI
- Interfaz digital de instrumentar música (MIDI), cambiar volumen
- MIDI (Interfaz digital de instrumentar música), cambiar volumen
- reproducir archivos MIDI, cambiar volumen
- cambiar el volumen DE MES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272319"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Cambiar el volumen interno del sintetizador de MIDI

Windows proporciona las siguientes funciones para recuperar y establecer el nivel de volumen de los dispositivos de sintetizador INTERNO de MIDI:



| Value                                        | Significado                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera el nivel de volumen del dispositivo de sintetizador INTERNO DE MIDI especificado. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Establece el nivel de volumen del dispositivo de sintetizador INTERNO DE MIDI especificado.      |



 

No todos los dispositivos de salida MIDI admiten cambios de volumen. Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho. Para obtener información sobre cómo determinar si un dispositivo determinado admite cambios de volumen, vea [Consulta de dispositivos de salida DE MIDI.](querying-midi-output-devices.md)

A menos que la aplicación esté diseñada para ser una aplicación maestra de control de volumen (proporciona al usuario control de volumen para todos los dispositivos de audio de un sistema), debe abrir un dispositivo de audio antes de cambiar su volumen. También debe comprobar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.

El volumen se especifica como un valor doubleword. Los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.

En el caso de los dispositivos que no admiten cambios de volumen individuales en los canales izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y los 16 bits superiores se omiten. Los valores del nivel de volumen van 0x0 (silencio) a 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento de volumen percibido es el mismo al aumentar el nivel de volumen de 0x5000 a 0x6000, ya que va de 0x4000 a 0x5000.

 

 