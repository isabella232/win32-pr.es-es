---
title: Cambiar el volumen de Audio-Devices auxiliares
description: Cambiar el volumen de Audio-Devices auxiliares
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio de una onda, cambio del volumen del dispositivo de audio auxiliar
- cambiar el volumen del dispositivo de audio auxiliar
- audio auxiliar, cambio del volumen del dispositivo
- interfaz de audio auxiliar
- dispositivos de audio auxiliares, cambiar volumen
- audio auxiliar, interfaz
- audio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791638"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Cambiar el volumen de Audio-Devices auxiliares

Windows proporciona las siguientes funciones para consultar y establecer el volumen de los dispositivos de audio auxiliares.



| Función                             | Descripción                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Recupera la configuración del volumen actual del dispositivo de salida auxiliar especificado. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Establece el volumen del dispositivo de salida auxiliar especificado.                      |



 

No todos los dispositivos de audio auxiliares admiten cambios de volumen. Algunos dispositivos pueden admitir cambios de volumen individuales en los canales izquierdo y derecho.

El volumen se especifica en un valor palabra, al igual que con las funciones de control de volumen de onda y audio de forma de onda. Cuando el formato de audio es estéreo, los 16 bits superiores especifican el volumen relativo del canal derecho y los 16 bits inferiores especifican el volumen relativo del canal izquierdo. En el caso de los dispositivos que no admiten el control de volumen de canal izquierdo y derecho, los 16 bits inferiores especifican el nivel de volumen y se omiten los 16 bits superiores.

Los valores de nivel de volumen van desde 0X0 (silencio) hasta 0xFFFF (volumen máximo) y se interpretan logarítmicamente. El aumento del volumen percibido es el mismo cuando se aumenta el nivel de volumen de 0x5000 a 0x6000, ya que es de 0x4000 a 0x5000.

 

 