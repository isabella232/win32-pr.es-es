---
title: Cambiar el volumen del sintetizador MIDI interno
description: Cambiar el volumen del sintetizador MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Interfaz digital de instrumentos musicales (MIDI), sintetizadores internos
- MIDI (interfaz digital de instrumentos musicales), sintetizadores internos
- reproducir archivos MIDI, sintetizadores internos
- Sintetizadores MIDI internos
- Interfaz digital de instrumentos musicales (MIDI), cambio de volumen
- MIDI (interfaz digital de instrumentos musicales), cambio de volumen
- reproducir archivos MIDI, cambiar el volumen
- cambiar el volumen MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995225"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Cambiar el volumen del sintetizador MIDI interno

Windows proporciona las siguientes funciones para recuperar y establecer el nivel de volumen de los dispositivos de sintetizador MIDI internos:



| Value                                        | Significado                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera el nivel de volumen del dispositivo de sintetizador MIDI interno especificado. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Establece el nivel de volumen del dispositivo de sintetizador MIDI interno especificado.      |



 

No todos los dispositivos de salida MIDI admiten cambios de volumen. Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho. Para obtener información sobre cómo determinar si un dispositivo determinado admite cambios de volumen, consulte [consultar los dispositivos de salida MIDI](querying-midi-output-devices.md).

A menos que la aplicación esté diseñada para ser una aplicación de control de volumen principal (proporciona al usuario control de volumen para todos los dispositivos de audio de un sistema), debe abrir un dispositivo de audio antes de cambiar su volumen. También debe comprobar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.

El volumen se especifica como un valor de palabra. Los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo.

En el caso de los dispositivos que no admiten cambios de volumen individuales en los canales izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores. Los valores para el intervalo de nivel de volumen desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.

 

 