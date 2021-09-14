---
title: Detener, pausar y reiniciar la reproducción
description: Detener, pausar y reiniciar la reproducción
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio de onda, detención de la reproducción
- interfaz de audio de onda, detener la reproducción
- reproducir archivos de audio de forma de onda, detener la reproducción
- audio de onda, pausar la reproducción
- interfaz audio-forma de onda, pausar la reproducción
- reproducir archivos de audio de forma de onda, pausar la reproducción
- audio de forma de onda, reinicio de la reproducción
- interfaz de audio de onda, reinicio de la reproducción
- reproducir archivos de audio de forma de onda, reiniciar la reproducción
- función waveOutPause
- waveOutReset (función)
- waveOutRestart (función)
- detener la reproducción de audio con forma de onda
- pausar la reproducción de audio de forma de onda
- reiniciar la reproducción de audio con forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260828"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Detener, pausar y reiniciar la reproducción

Puede detener o pausar la reproducción mientras se reproduce el audio de forma de onda. Después de pausar la reproducción, puede reiniciarla. Windows proporciona las siguientes funciones para controlar la reproducción de audio de forma de onda.



| Función                                 | Descripción                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Pausa la reproducción en un dispositivo de salida de audio de forma de onda.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Detiene la reproducción en un dispositivo de salida de audio de forma de onda y marca todos los bloques de datos pendientes como se ha hecho. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Reanuda la reproducción en un dispositivo de salida de audio de forma de onda pausado.                                  |



 

Pausar un dispositivo de audio de forma de onda mediante [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) podría no ser instantáneo; El controlador puede terminar de reproducir el bloque actual antes de pausar la reproducción.

Por lo general, en cuanto se envía el primer bloque de datos de audio de forma de onda mediante la función [**waveOutWrite,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) el dispositivo de audio de forma de onda comienza a reproducirse. Si no desea que el sonido empiece a reproducirse inmediatamente, llame a **waveOutPause** antes de llamar **a waveOutWrite**. A continuación, cuando quiera empezar a reproducir datos de audio de forma de onda, llame [**a waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

No se puede **usar waveOutRestart para** reiniciar un dispositivo que se ha detenido con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); debe usar **waveOutWrite para** enviar el primer bloque de datos para reanudar la reproducción en el dispositivo.

 

 