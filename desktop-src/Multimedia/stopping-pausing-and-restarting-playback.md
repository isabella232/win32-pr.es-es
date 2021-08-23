---
title: Detener, pausar y reiniciar la reproducción
description: Detener, pausar y reiniciar la reproducción
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio de forma de onda, detención de la reproducción
- interfaz audio-forma de onda, detener la reproducción
- reproducir archivos de audio de forma de onda, detener la reproducción
- audio de forma de onda, pausar la reproducción
- interfaz de audio de forma de onda, pausar la reproducción
- reproducir archivos de audio de forma de onda, pausar la reproducción
- audio de forma de onda, reinicio de la reproducción
- interfaz de audio de forma de onda, reinicio de la reproducción
- reproducir archivos de audio de forma de onda, reiniciar la reproducción
- función waveOutPause
- Función waveOutReset
- waveOutRestart (función)
- detener la reproducción de audio de forma de onda
- pausar la reproducción de audio de forma de onda
- reiniciar la reproducción de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04491a676a104e288d274da7dd70eb759e363adc6476805b261a9651444bf1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688495"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Detener, pausar y reiniciar la reproducción

Puede detener o pausar la reproducción mientras se reproduce audio de forma de onda. Una vez pausada la reproducción, puede reiniciarla. Windows proporciona las siguientes funciones para controlar la reproducción de audio de forma de onda.



| Función                                 | Descripción                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Pausa la reproducción en un dispositivo de salida de audio de forma de onda.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Detiene la reproducción en un dispositivo de salida de audio de forma de onda y marca todos los bloques de datos pendientes como se ha hecho. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Reanuda la reproducción en un dispositivo de salida de audio de forma de onda pausado.                                  |



 

La pausa de un dispositivo de audio de forma de onda mediante [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) podría no ser instantánea; El controlador puede terminar de reproducir el bloque actual antes de pausar la reproducción.

Por lo general, en cuanto se envía el primer bloque de datos de audio de forma de onda mediante la función [**waveOutWrite,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) el dispositivo de audio de forma de onda comienza a reproducirse. Si no desea que el sonido empiece a reproducirse inmediatamente, llame a **waveOutPause** antes de llamar **a waveOutWrite**. A continuación, cuando quiera empezar a reproducir datos de audio de forma de onda, llame [**a waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

No puede usar **waveOutRestart para** reiniciar un dispositivo que se ha detenido con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); debe usar **waveOutWrite para** enviar el primer bloque de datos para reanudar la reproducción en el dispositivo.

 

 