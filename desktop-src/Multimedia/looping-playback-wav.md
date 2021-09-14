---
title: Reproducción en bucle (audio de forma de onda)
description: Reproducción en bucle (audio de forma de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio de forma de onda, sonidos de bucle
- interfaz audio-forma de onda, sonidos de bucle
- audio de forma de onda, reproducción en bucle
- interfaz de audio de onda, reproducción en bucle
- bucles de sonidos de audio de forma de onda
- bucle de reproducción de audio de forma de onda
- función waveOutWrite
- función waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173657"
---
# <a name="looping-playback"></a>Reproducción en bucle

Los miembros **dwLoops** y **dwFlags** de las estructuras [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que se pasan al dispositivo con la [**función waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) controlan el bucle de un sonido. Use las **marcas \_ WHDR BEGINLOOP** y **WHDR \_ ENDLOOP** del **miembro dwFlags** para especificar los bloques de datos inicial y final para el bucle.

Para recorrer en bucle un único bloque de datos, especifique ambas marcas para el mismo bloque. Para especificar el número de bucles, use el **miembro dwLoops** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para el primer bloque del bucle.

Puede llamar a la [**función waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para detener un sonido de bucle.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducir Waveform-Audio archivos](playing-waveform-audio-files.md)
</dt> </dl>

 

 
