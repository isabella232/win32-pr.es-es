---
title: Cambiar el tono y la velocidad de reproducción
description: Cambiar el tono y la velocidad de reproducción
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio de forma de onda, tono
- interfaz de audio de forma de onda, pitch
- audio de forma de onda, velocidad de reproducción
- interfaz de audio de forma de onda, velocidad de reproducción
- audio de forma de onda, cambio de tono
- interfaz de audio de forma de onda, cambio de tono
- audio de forma de onda, cambio de velocidad de reproducción
- interfaz de audio de forma de onda, cambiar la velocidad de reproducción
- cambiar la velocidad de reproducción de audio de forma de onda
- cambiar el tono de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006788c286476434a7ca2a3d5b79dbd6c4d8af431d74ffb4a00e03a7357777f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941283"
---
# <a name="changing-pitch-and-playback-rate"></a>Cambiar el tono y la velocidad de reproducción

Algunos dispositivos de salida de audio de forma de onda pueden variar el tono y la velocidad de reproducción de los datos de audio de forma de onda. No todos los dispositivos de audio de forma de onda admiten cambios de tono y velocidad de reproducción. Para obtener información sobre cómo determinar si un dispositivo de audio de forma de onda determinado admite cambios de tono y velocidad de reproducción, vea [Dispositivos y tipos de datos](devices-and-data-types.md).

Las diferencias entre cambiar el tono y la velocidad de reproducción son las siguientes:

-   El controlador del dispositivo realiza el cambio de la velocidad de reproducción y no requiere hardware especializado. La frecuencia de muestreo no cambia, pero el controlador interpola omitiendo o sintetizando muestras. Por ejemplo, si la velocidad de reproducción cambia por un factor de dos, el controlador omite todas las demás muestras.
-   El cambio de tono requiere hardware especializado. La velocidad de reproducción y la frecuencia de muestreo no se cambian.

Windows proporciona las siguientes funciones para consultar y establecer velocidades de reproducción y tono de audio de forma de onda.



| Función                                                 | Descripción                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Recupera el tono para el dispositivo de salida de audio de forma de onda especificado.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Recupera la velocidad de reproducción del dispositivo de salida de audio de forma de onda especificado. |
| [**waveOutSetPjunto**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Establece el tono para el dispositivo de salida de audio de forma de onda especificado.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Establece la velocidad de reproducción del dispositivo de salida de audio de forma de onda especificado.      |



 

Las velocidades de inclinación y reproducción cambian por un factor especificado con un número de punto fijo empaquetado en un valor doubleword. Los 16 bits superiores especifican la parte entera del número; los 16 bits inferiores especifican la parte fraccionera. Por ejemplo, el valor 1.5 se representa como 0x00018000L. El valor 0,75 se representa como 0x0000C000L. Un valor de 1,0 (0x00010000) significa que la velocidad de inclinación o reproducción no cambia.

 

 