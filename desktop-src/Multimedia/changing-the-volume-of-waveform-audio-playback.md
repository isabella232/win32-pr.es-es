---
title: Cambiar el volumen de la Waveform-Audio reproducción
description: Cambiar el volumen de la Waveform-Audio reproducción
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio de forma de onda, cambio del volumen de reproducción
- interfaz de audio de forma de onda, cambio del volumen de reproducción
- audio de forma de onda, volumen de reproducción
- interfaz de audio de forma de onda, volumen de reproducción
- cambiar el volumen de reproducción de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807995"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Cambiar el volumen de la Waveform-Audio reproducción

Windows proporciona las siguientes funciones para consultar y establecer el nivel de volumen de los dispositivos de salida de audio de forma de onda.



| Función                                     | Descripción                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Recupera el nivel de volumen actual del dispositivo de salida de audio de forma de onda especificado. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Establece el nivel de volumen del dispositivo de salida de audio de forma de onda especificado.              |



 

No todos los dispositivos de audio de forma de onda admiten cambios de volumen. Algunos dispositivos admiten el control de volumen individual en los canales izquierdo y derecho. Para obtener información sobre cómo determinar las funcionalidades de control de volumen de los dispositivos de audio de forma de onda, vea [Dispositivos y tipos de datos](devices-and-data-types.md).

Algunas aplicaciones permiten al usuario controlar el volumen de todos los dispositivos de audio de un sistema. (Muchas aplicaciones de este tipo usan los servicios de mezclador de audio; para obtener más información, vea [Mezcladores de audio).](audio-mixers.md) A menos que la aplicación sea capaz de este tipo de control de volumen maestro, debe abrir un dispositivo de audio antes de cambiar su volumen. También debe consultar el nivel de volumen antes de cambiarlo y restaurar el nivel de volumen a su nivel anterior lo antes posible.

El volumen se especifica en un valor doubleword. Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo. En el caso de los dispositivos que no admiten el control de volumen del canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y los 16 bits superiores se omiten.

Los valores de nivel de volumen van 0x0 (silencio) a 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento del volumen percibido es el mismo al aumentar el nivel de volumen de 0x5000 a 0x6000 que de 0x4000 a 0x5000.

 

 