---
title: Reproducción en bucle (audio de forma de onda)
description: Reproducción en bucle (audio de forma de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio de forma de onda, sonidos de bucle
- interfaz de audio de forma de onda, bucles de sonidos
- audio de forma de onda, reproducción en bucle
- interfaz de audio de forma de onda, reproducción en bucle
- bucles de sonidos de audio de forma de onda
- bucle de reproducción de audio de forma de onda
- función waveOutWrite
- Función waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371216"
---
# <a name="looping-playback"></a>Reproducción en bucle

Los miembros **dwLoops** y **dwFlags** de las estructuras [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que se pasan al dispositivo con la [**función waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) controlan el bucle de un sonido. Use las **marcas \_ BEGINLOOP** y **WHDR \_ ENDLOOP** de WHDR en el miembro **dwFlags** para especificar los bloques de datos inicial y final para el bucle.

Para crear un bucle de un único bloque de datos, especifique ambas marcas para el mismo bloque. Para especificar el número de bucles, use el **miembro dwLoops** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para el primer bloque del bucle.

Puede llamar a la [**función waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para detener un sonido de bucle.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducir Waveform-Audio archivos](playing-waveform-audio-files.md)
</dt> </dl>

 

 
