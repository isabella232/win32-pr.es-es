---
title: Detener, pausar y reiniciar la reproducción
description: Detener, pausar y reiniciar la reproducción
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio de onda, Detener reproducción
- 'onda: interfaz de audio, Detener reproducción'
- reproducir los archivos de audio de onda, detener la reproducción
- audio de onda, pausar reproducción
- 'onda: interfaz de audio, pausar reproducción'
- reproducir archivos de audio de onda, pausar la reproducción
- audio de la onda, reinicio de la reproducción
- 'onda: interfaz de audio, reinicio de la reproducción'
- reproducir los archivos de audio de onda, reiniciando la reproducción
- waveOutPause función)
- waveOutReset función)
- waveOutRestart función)
- detención de la reproducción de audio de onda
- pausar la reproducción de onda-audio
- reinicio de la reproducción de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149199"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Detener, pausar y reiniciar la reproducción

Puede detener o pausar la reproducción mientras se reproduce el audio de forma de onda. Una vez que se haya pausado la reproducción, puede reiniciarla. Windows proporciona las siguientes funciones para controlar la reproducción de audio de una onda.



| Función                                 | Descripción                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Pausa la reproducción en un dispositivo de salida de onda-audio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Detiene la reproducción en un dispositivo de salida de onda-audio y marca todos los bloques de datos pendientes como terminados. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Reanuda la reproducción en un dispositivo de salida de audio de onda en pausa.                                  |



 

Pausar un dispositivo de audio de forma de onda mediante [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) puede no ser instantáneo; el controlador puede acabar de reproducir el bloque actual antes de pausar la reproducción.

Generalmente, en cuanto se envía el primer bloque de datos de audio de forma de onda mediante la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , el dispositivo de audio de forma de onda comienza a reproducirse. Si no desea que el sonido empiece a reproducirse inmediatamente, llame a **waveOutPause** antes de llamar a **waveOutWrite**. A continuación, cuando desee comenzar a reproducir datos de audio de onda, llame a [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

No se puede usar **waveOutRestart** para reiniciar un dispositivo detenido con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset). debe usar **waveOutWrite** para enviar el primer bloque de datos para reanudar la reproducción en el dispositivo.

 

 