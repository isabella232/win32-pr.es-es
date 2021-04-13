---
title: Recuperar la posición de reproducción actual
description: Recuperar la posición de reproducción actual
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio de forma de onda, posición de reproducción actual
- 'forma de onda: interfaz de audio, posición de reproducción actual'
- reproducción de forma de onda-archivos de audio, posición de reproducción actual
- waveOutGetPosition función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358820"
---
# <a name="retrieving-the-current-playback-position"></a>Recuperar la posición de reproducción actual

Puede supervisar la posición de reproducción actual dentro del archivo mientras se reproduce el audio de forma de onda mediante la función [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .

En el caso de los dispositivos de audio de forma de onda, los ejemplos son el formato de hora preferido en el que se representa la posición actual. Por lo tanto, la posición actual de un dispositivo de audio de forma de onda se especifica como el número de muestras de un canal desde el principio del archivo de audio de forma de onda. Para consultar la posición actual de un dispositivo de audio de forma de onda, establezca el miembro **wType** de la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) en ejemplos de tiempo \_ y pase esta estructura a **waveOutGetPosition**.

La estructura **MMTIME** puede representar el tiempo en uno o varios formatos diferentes, incluidos los milisegundos, ejemplos, SMPTE (sociedad de los ingenieros de cine y televisión) y formatos de puntero de canción MIDI. El miembro **wType** especifica el formato que se usa para representar la hora. Antes de llamar a una función que usa la estructura **MMTIME** , debe establecer **wType** para indicar el formato de hora solicitado. Asegúrese de comprobar **wType** después de la llamada para ver si se admite el formato de hora solicitado. Si no se admite el formato de hora solicitado, el controlador de dispositivo especifica la hora en un formato de hora alternativo y cambia el miembro de **wType** al formato de hora seleccionado.

Para obtener más información sobre la estructura **MMTIME** , vea [temporizadores multimedia](multimedia-timers.md).

 

 