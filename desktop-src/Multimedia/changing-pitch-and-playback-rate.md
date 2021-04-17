---
title: Cambiar la velocidad de reproducción y el tono
description: Cambiar la velocidad de reproducción y el tono
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio de una onda, paso
- 'onda: interfaz de audio, paso'
- audio de onda, velocidad de reproducción
- 'onda: interfaz de audio, velocidad de reproducción'
- audio de una onda, cambiar el tono
- 'onda: interfaz de audio, cambio de tono'
- audio de onda, cambio de velocidad de reproducción
- 'onda: interfaz de audio, cambio de velocidad de reproducción'
- cambiar la velocidad de reproducción de audio de onda
- cambiar onda-tono de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487723"
---
# <a name="changing-pitch-and-playback-rate"></a>Cambiar la velocidad de reproducción y el tono

Algunos dispositivos de salida de onda-audio pueden variar el paso y la velocidad de reproducción de los datos de audio de onda. No todos los dispositivos de audio de onda admiten cambios de tono y de velocidad de reproducción. Para obtener información sobre cómo determinar si un dispositivo de audio de forma de onda determinado admite cambios de velocidad y de reproducción, consulte [dispositivos y tipos de datos](devices-and-data-types.md).

Las diferencias entre cambiar el tono y la velocidad de reproducción son las siguientes:

-   El controlador de dispositivo realiza el cambio de la velocidad de reproducción y no requiere hardware especializado. La velocidad de muestra no cambia, pero el controlador se interpola omitiendo o sintetizando ejemplos. Por ejemplo, si se cambia la velocidad de reproducción en un factor de dos, el controlador omite cada ejemplo.
-   Cambiar el tono requiere hardware especializado. La velocidad de reproducción y la velocidad de muestreo no cambian.

Windows proporciona las siguientes funciones para consultar y establecer las frecuencias de reproducción y paso de audio y de onda.



| Función                                                 | Descripción                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Recupera el tono para el dispositivo de salida de audio de onda especificado.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Recupera la velocidad de reproducción para el dispositivo de salida de audio de onda especificado. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Establece el tono para el dispositivo de salida de audio de onda especificado.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Establece la velocidad de reproducción para el dispositivo de salida de audio de onda especificado.      |



 

Las tasas de paso y reproducción se cambian mediante un factor especificado con un número de punto fijo empaquetado en un valor de palabra. Los 16 bits superiores especifican la parte entera del número; los 16 bits inferiores especifican la parte fraccionaria. Por ejemplo, el valor 1,5 se representa como 0x00018000L. El valor 0,75 se representa como 0x0000C000L. Un valor de 1,0 (0x00010000) significa que el paso o la velocidad de reproducción no cambian.

 

 