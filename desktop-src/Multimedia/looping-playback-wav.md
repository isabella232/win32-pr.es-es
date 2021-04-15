---
title: Reproducción en bucle (audio de onda)
description: Reproducción en bucle (audio de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio de una onda, sonidos en bucle
- 'onda: interfaz de audio, sonidos en bucle'
- audio de una onda, reproducción en bucle
- 'onda: interfaz de audio, reproducción en bucle'
- 'onda de onda de bucle: sonidos de audio'
- 'onda en bucle: reproducción de audio'
- waveOutWrite función)
- waveOutBreakLoop función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105654027"
---
# <a name="looping-playback"></a>Reproducción en bucle

El bucle de un sonido lo controlan los miembros **dwLoops** y **dwFlags** en las estructuras [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que se pasan al dispositivo con la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . Use las marcas **WHDR \_ BEGINLOOP** y **WHDR \_ ENDLOOP** en el miembro **dwFlags** para especificar los bloques de datos inicial y final para el bucle.

Para recorrer un solo bloque de datos, especifique ambos marcadores para el mismo bloque. Para especificar el número de bucles, utilice el miembro **dwLoops** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para el primer bloque del bucle.

Puede llamar a la función [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para detener un sonido de bucle.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducir archivos Waveform-Audio](playing-waveform-audio-files.md)
</dt> </dl>

 

 
