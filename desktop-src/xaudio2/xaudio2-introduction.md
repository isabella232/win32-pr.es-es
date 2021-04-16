---
description: XAudio2 es una API de audio de bajo nivel. Proporciona una base de procesamiento de señal y combinación para juegos similares a sus predecesores, DirectSound y XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Introducción a XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7cde958256d9126746a07764dc0c792e88289c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720746"
---
# <a name="xaudio2-introduction"></a>Introducción a XAudio2

XAudio2 es una API de audio de bajo nivel. Proporciona una base de procesamiento de señal y combinación para juegos similares a sus predecesores, DirectSound y XAudio.

XAudio2 es el sustituto de larga duración de DirectSound. Aborda varios problemas pendientes y solicitudes de características.

## <a name="xaudio2-features"></a>Características de XAudio2

A continuación se muestra una lista de las características de XAudio2 y la nueva funcionalidad que permite a los desarrolladores mejorar el rendimiento de sus juegos.

-   Efectos de DSP y filtrado por voz

    Los efectos de procesamiento de señal digital (DSP) son los sombreadores de píxeles de audio. Controlan todo, desde la transformación de un sonido, convirtiéndolo en un squeal de Pig a un bajo sonido de un poco de miedo, para colocar sonidos en el entorno de juego mediante el filtrado de reverberación y oclusión o obstrucción. XAudio2 proporciona un marco DSP flexible y eficaz. También proporciona un filtro integrado en cada voz, para efectos eficaces de filtrado de paso bajo/alto/banda-paso.

    Consulte [efectos de audio de XAudio2](xaudio2-audio-effects.md) y [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para obtener más información sobre los efectos de DSP y el filtrado por voz.

-   Submezcla

    La submezcla combina varios sonidos en una única secuencia de audio, por ejemplo, un sonido de motor compuesto por partes compuestas, que se reproducen simultáneamente. Además, puede usar la submezcla para procesar y combinar partes similares de un juego. Por ejemplo, puede combinar todos los efectos sonoros de juego para permitir que se aplique una configuración de volumen de usuario mientras una configuración independiente controla el volumen de música. Combinado con DSP, la submezcla proporciona el tipo de enrutamiento de datos y el procesamiento necesario para los juegos de hoy en día. XAudio2 permite niveles arbitrarios de submezcla, lo que permite la creación de sonidos y mezclas de juegos complejos.

    Consulte [gráfico de audio de xaudio2](xaudio2-audio-graph.md) y [voces de xaudio2](xaudio2-voices.md) para obtener más información sobre la submezcla.

-   Compatibilidad con audio comprimido

    Una de las principales solicitudes de características de DirectSound ha sido la compatibilidad con audio comprimido. XAudio2 admite formatos comprimidos (ADPCM) de forma nativa con la descompresión en tiempo de ejecución.

-   Compatibilidad con multicanal y sonido envolvente mejorado

    Se amplía la compatibilidad con multicanal, 3D y sonido envolvente. 3D y el sonido envolvente son ahora mucho más flexibles y transparentes. XAudio2 quita el límite de 6 canales de los sonidos multicanal y admite audio multicanal en cualquier tarjeta de audio compatible con multicanal. No es necesario que la tarjeta se acelere por hardware.

-   Procesamiento de velocidad

    Para ayudar a minimizar el uso de CPU, XAudio2 proporciona la tecnología para crear varios gráficos de procesamiento de audio de baja velocidad. Esto puede reducir significativamente el uso de CPU al permitir que un juego procese audio a la velocidad del material de origen si la velocidad es inferior a 48 kHz.

-   Modelo de API sin bloqueos

    Con pocas excepciones, una llamada al método XAudio2 no bloqueará el motor de procesamiento de audio. Esto significa que un cliente puede realizar un conjunto de llamadas a métodos de forma segura en cualquier momento sin bloquear llamadas de ejecución prolongada que producen retrasos. Las excepciones son el método [**IXAudio2Voice::D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (que puede bloquear el motor hasta que la voz que se está destruyendo finaliza el procesamiento) y los métodos que finalizan el subproceso de audio: [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) y [**IXAudio2:: Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Tenga en cuenta que, mientras que las llamadas al método de XAudio2 no bloquearán el motor de procesamiento de audio, los métodos de XAudio2 contienen secciones críticas y se pueden bloquear en algunas circunstancias.

## <a name="when-to-use-xaudio2"></a>Cuándo usar XAudio2

XAudio2 está pensado principalmente para desarrollar motores de audio de alto rendimiento para juegos. Para los desarrolladores de juegos que quieren agregar efectos de sonido y música de fondo a sus juegos modernos, XAudio2 ofrece un motor de mezcla de gráfico de audio con baja latencia y compatibilidad con búferes dinámicos, reproducción sincrónica fiel a la muestra y conversión implícita de velocidad de origen. En comparación con WASAPI, XAudio2 solo requiere una cantidad mínima de código, incluso para soluciones de audio complejas. En comparación con el motor de Media Foundation, XAudio2 es una API de C++ de baja latencia y bajo nivel que está diseñada para su uso en juegos.

En el caso de las aplicaciones que simplemente necesitan una reproducción de música normal, el motor de Media Foundation puede ser una coincidencia mejor con los requisitos de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
