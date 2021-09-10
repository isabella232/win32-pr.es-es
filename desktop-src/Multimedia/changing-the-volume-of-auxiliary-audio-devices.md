---
title: Cambiar el volumen de la Audio-Devices
description: Cambiar el volumen de la Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio de forma de onda, cambio del volumen auxiliar del dispositivo de audio
- cambiar el volumen del dispositivo de audio auxiliar
- audio auxiliar, cambio del volumen del dispositivo
- interfaz de audio auxiliar
- dispositivos de audio auxiliares, cambio de volumen
- audio auxiliar, interfaz
- audio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371276"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Cambiar el volumen de la Audio-Devices

Windows proporciona las siguientes funciones para consultar y establecer el volumen de los dispositivos de audio auxiliares.



| Función                             | Descripción                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Recupera la configuración de volumen actual del dispositivo de salida auxiliar especificado. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Establece el volumen del dispositivo de salida auxiliar especificado.                      |



 

No todos los dispositivos de audio auxiliares admiten cambios de volumen. Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho.

El volumen se especifica en un valor doubleword, al igual que con las funciones de control de volumen de audio de forma de onda y MIDI. Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo. En el caso de los dispositivos que no admiten el control de volumen del canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y los 16 bits superiores se omiten.

Los valores de nivel de volumen van 0x0 (silencio) a 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento de volumen percibido es el mismo al aumentar el nivel de volumen de 0x5000 a 0x6000 que de 0x4000 a 0x5000.

 

 