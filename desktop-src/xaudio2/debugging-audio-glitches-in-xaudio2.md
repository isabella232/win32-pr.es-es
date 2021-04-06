---
description: Se pueden producir problemas en XAudio2, en este tema se explica cómo se informan y algunos enfoques para corregirlos.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurar problemas de audio en XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911113"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Depurar problemas de audio en XAudio2

Se pueden producir problemas en XAudio2, en este tema se explica cómo se informan y algunos enfoques para corregirlos.

En esta información general se tratan los temas siguientes:

-   [Causas de problemas o problemas de salida de audio](#causes-of-audio-output-problems-or-glitches)
-   [Cómo notifica XAudio2 los problemas](#how-xaudio2-reports-problems)
-   [Enfoques para solucionar problemas](#approaches-to-fixing-problems)
-   [Temas relacionados](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Causas de problemas o problemas de salida de audio

Los problemas pueden producirse en la salida de XAudio2 por varios motivos.

-   Se ha agotado una voz de origen de XAudio2. El cliente no envía un audio nuevo a él lo suficientemente rápido. Obtiene el silencio porque no tiene datos para reproducir.
-   En conjunto, XAudio2 se sobrecarga. Tarda más de *x* MS en producir *x* MS de audio. Obtiene las faltas porque XAudio2 no puede producir datos tan rápido como el dispositivo de audio lo necesita. Puede que esté ejecutando demasiadas voces o efectos a la vez, haciendo demasiado trabajo en las devoluciones de llamada de XAudio2 o realizando llamadas a la API de XAudio2 con demasiada frecuencia.
-   El subproceso de procesamiento de audio se está deteniendo porque la implementación del cliente de alguna devolución de llamada de XAudio2 está realizando cosas que pueden bloquear el subproceso. Por ejemplo, podría tener acceso al disco, sincronizar con otros subprocesos o llamar a otras funciones que se puedan bloquear. Utilice un subproceso en segundo plano de prioridad inferior que la devolución de llamada pueda señalizar para realizar dichas tareas.
-   El sistema en su conjunto está sobrecargado. Otros subprocesos que se ejecutan con la misma prioridad o mayor que XAudio2 están haciendo demasiado trabajo. Compiten con el subproceso de audio para el tiempo de CPU.

## <a name="how-xaudio2-reports-problems"></a>Cómo notifica XAudio2 los problemas

XAudio2 puede comunicar los problemas de la compilación de depuración de varias maneras.

-   Si se ha agotado una voz, XAudio2 muestra un mensaje en este formulario.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Si el subproceso de audio se ejecuta durante demasiado tiempo, XAudio2 muestra un mensaje en este formulario.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    Normalmente, este mensaje aparece con el siguiente mensaje.

-   Si el controlador de audio no puede alimentar nuevos datos de audio en el tiempo, XAudio2 muestra un mensaje en este formulario.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   La llamada a [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) proporciona datos de rendimiento de XAudio2, incluido el número total de problemas desde que se inició el motor de xaudio2.

## <a name="approaches-to-fixing-problems"></a>Enfoques para solucionar problemas

Las formas posibles de reducir los problemas de audio son las siguientes.

-   En el caso del agotamiento de la voz: aumente la cantidad de datos de audio que se ponen en cola en una voz. Puede usar [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para detectar el número de búferes en cola en cualquier momento. Si sigue viendo errores de inanición de voz, pero no puede oír ningún problema, asegúrese de que está estableciendo el [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Marcas** para \_ el fin \_ de \_ la secuencia de XAUDIO2 en el búfer final de un sonido. Esto indica a XAudio2 que no espere que más búferes estén disponibles en cuanto se complete.

    En los demás casos:

    -   Reduzca el número de voces y efectos activos en el gráfico, especialmente efectos costosos como reverberación.
    -   Deshabilite las voces y los efectos que no esté usando.
    -   Use las \_ \_ marcas de voz NOSRC y xaudio2 Voice \_ de xaudio2 \_ en [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), siempre que sea posible. La conversión de la frecuencia de muestreo es costosa.
    -   Reduzca la velocidad de muestra de las voces individuales. Por ejemplo, una voz de submezcla que hospeda un efecto de reverberación puede tener una velocidad de muestra menor que la voz de origen que envía a ella. Los sonidos como explosiones y gunshots que no necesitan alta fidelidad también se pueden grabar a velocidades de muestra inferiores.
    -   Asegúrese de que las implementaciones de devolución de llamada hacen tan poco trabajo como sea posible y no bloqueen nunca.
    -   Realice menos llamadas a XAudio2. Normalmente no es necesario actualizar los parámetros de audio para cada fotograma de vídeo. Cada 30 ms es suficiente. Debe eliminar las llamadas redundantes, como establecer el volumen varias veces en una sucesión rápida.
    -   Reduzca el uso general de la CPU del juego.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de depuración](debugging-facilities.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
