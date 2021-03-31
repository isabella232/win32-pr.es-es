---
title: Cambiar el volumen de la reproducción de Waveform-Audio
description: Cambiar el volumen de la reproducción de Waveform-Audio
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio de una onda, cambio del volumen de reproducción
- 'onda: interfaz de audio, cambio del volumen de reproducción'
- audio de onda, volumen de reproducción
- 'onda: interfaz de audio, volumen de reproducción'
- cambiar el volumen de reproducción de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791637"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Cambiar el volumen de la reproducción de Waveform-Audio

Windows proporciona las siguientes funciones para consultar y establecer el nivel de volumen de los dispositivos de salida de onda y audio.



| Función                                     | Descripción                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Recupera el nivel de volumen actual del dispositivo de salida de forma de onda especificado. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Establece el nivel de volumen del dispositivo de salida de onda-audio especificado.              |



 

No todos los dispositivos de audio de onda admiten cambios de volumen. Algunos dispositivos admiten el control de volumen individual en los canales izquierdo y derecho. Para obtener información sobre cómo determinar las capacidades de control de volumen de los dispositivos de audio de forma de onda, consulte [dispositivos y tipos de datos](devices-and-data-types.md).

Algunas aplicaciones permiten al usuario controlar el volumen de todos los dispositivos de audio de un sistema. (Muchas aplicaciones de este tipo usan los servicios de mezclador de audio; para obtener más información, consulte [mezcladores de audio](audio-mixers.md)). A menos que la aplicación sea capaz de realizar este tipo de control de volumen maestro, debe abrir un dispositivo de audio antes de cambiar su volumen. También debe consultar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.

El volumen se especifica en un valor de palabra. Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo. En el caso de los dispositivos que no admiten el control de volumen de canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores.

Los valores de nivel de volumen van desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.

 

 