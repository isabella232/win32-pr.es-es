---
description: Los problemas pueden producirse en XAudio2, en este tema se explica cómo se notifican y algunos enfoques para corregirlos.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurar problemas de audio en XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8856defc67bc9453b9d83f5ed369bfb96f48b8c2c16c92ea535a0c1b648402b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703625"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Depurar problemas de audio en XAudio2

Los problemas pueden producirse en XAudio2, en este tema se explica cómo se notifican y algunos enfoques para corregirlos.

En esta introducción se tratan los temas siguientes:

-   [Causas de problemas de salida de audio o problemas](#causes-of-audio-output-problems-or-glitches)
-   [Cómo informa XAudio2 de problemas](#how-xaudio2-reports-problems)
-   [Enfoques para solucionar problemas](#approaches-to-fixing-problems)
-   [Temas relacionados](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Causas de problemas de salida de audio o problemas

Los problemas pueden producirse en la salida de XAudio2 por varias razones.

-   Una voz de origen XAudio2 se ha quedado. El cliente no le envía audio nuevo lo suficientemente rápido. Se obtiene el silencio porque no tiene datos para reproducir.
-   XAudio2 como un todo se sobrecarga. Se tarda más de *X* ms en generar *X* ms de audio. Se obtienen las eliminaciones porque XAudio2 no puede generar datos tan rápido como los necesite el dispositivo de audio. Es posible que esté ejecutando demasiadas voces o efectos a la vez, realizando demasiado trabajo en devoluciones de llamada de XAudio2 o realizando llamadas API de XAudio2 con demasiada frecuencia.
-   El subproceso de procesamiento de audio se está deteniendo porque la implementación del cliente de alguna devolución de llamada XAudio2 está haciendo cosas que pueden bloquear el subproceso. Por ejemplo, podría estar accediendo al disco, sincronizando con otros subprocesos o llamando a otras funciones que pueden bloquearse. Use un subproceso en segundo plano de prioridad inferior que la devolución de llamada pueda indicar para realizar dichas tareas.
-   El sistema en su conjunto está sobrecargado. Otros subprocesos que se ejecutan con la misma prioridad o mayor que XAudio2 están realizando demasiado trabajo. Compiten con el subproceso de audio por el tiempo de CPU.

## <a name="how-xaudio2-reports-problems"></a>Cómo informa XAudio2 de problemas

XAudio2 puede comunicar problemas en la compilación de depuración de varias maneras.

-   Si una voz se está pasando de inanición, XAudio2 muestra un mensaje con este formato.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Si el subproceso de audio se ejecuta durante demasiado tiempo, XAudio2 muestra un mensaje con este formato.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    Normalmente, este mensaje se produce con el siguiente mensaje.

-   Si el controlador de audio no se puede alimentar a tiempo con nuevos datos de audio, XAudio2 muestra un mensaje con este formato.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   Al [**llamar a IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) se proporcionan datos de rendimiento de XAudio2, incluido el número total de problemas desde que se inició el motor XAudio2.

## <a name="approaches-to-fixing-problems"></a>Enfoques para solucionar problemas

Entre las posibles formas de reducir los problemas de audio se incluyen las siguientes:

-   En el caso de la pérdida de voz: aumente la cantidad de datos de audio que se ponen en cola por adelantado en una voz. Puede usar [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para detectar el número de búferes en cola en cualquier momento. Si todavía ve errores de inanición de voz, pero no puede escuchar ningún problema, asegúrese de establecer [**buffer XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Marca a** XAUDIO2 \_ END OF STREAM en el búfer final de un \_ \_ sonido. Esto indica a XAudio2 que no espere que haya más búferes necesariamente disponibles en cuanto se complete este.

    En los demás casos:

    -   Reduzca el número de voces activas y efectos en el gráfico, especialmente los efectos costosos como la reverberación.
    -   Deshabilite las voces y los efectos que no está usando.
    -   Use las marcas XAUDIO2 VOICE NOSRC y \_ \_ XAUDIO2 \_ VOICE NOPITCH en \_ [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)siempre que sea posible. La conversión de frecuencia de muestreo es costosa.
    -   Reduzca la frecuencia de muestreo de las voces individuales. Por ejemplo, una submezcla de voz que hospeda un efecto de reverberación puede tener una frecuencia de muestreo menor que la voz de origen que se envía a ella. También se pueden grabar sonidos como las explosións y los impactos de pólver que no necesitan alta fidelidad a velocidades de muestra más bajas.
    -   Asegúrese de que las implementaciones de devolución de llamada funcionan lo menos posible y nunca se bloquean.
    -   Realice menos llamadas a XAudio2. Normalmente, no es necesario actualizar los parámetros de audio para cada fotograma de vídeo. Cada 30 ms o así es suficiente. Debe eliminar las llamadas redundantes, como establecer el volumen varias veces en una sucesión rápida.
    -   Reduzca el uso general de CPU del juego.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalaciones de depuración](debugging-facilities.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
