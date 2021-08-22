---
description: XAudio2 es una API de audio de bajo nivel. Proporciona una base de procesamiento y combinación de señales para juegos que es similar a sus predecesores, DirectSound y XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Introducción a XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a966e9682a7f605864c0374a588d4b7eb3724036fe284bd6d92c64080e9225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589905"
---
# <a name="xaudio2-introduction"></a>Introducción a XAudio2

XAudio2 es una API de audio de bajo nivel. Proporciona una base de procesamiento y combinación de señales para juegos que es similar a sus predecesores, DirectSound y XAudio.

XAudio2 es el reemplazo esperado para DirectSound. Aborda varios problemas pendientes y solicitudes de características.

## <a name="xaudio2-features"></a>Características de XAudio2

A continuación se muestra una lista de características de XAudio2 y nuevas funcionalidades que permiten a los desarrolladores mejorar el rendimiento de sus juegos.

-   Efectos de DSP y filtrado por voz

    Los efectos de Procesamiento de señales digitales (DSP) son los sombreadores de píxeles del audio. Se encargan de todo, desde la transformación de un sonido(convertir un sonido de pig en un sonido de sonido escalofrío bajo y extraño) hasta colocar sonidos en el entorno del juego mediante reverberación y oclusión o filtrado de obstáculos. XAudio2 proporciona un marco DE DSP flexible y eficaz. También proporciona un filtro integrado en cada voz, para obtener efectos eficaces de filtrado bajo, alto o de paso de banda.

    Vea Efectos de audio de [XAudio2](xaudio2-audio-effects.md) e [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para obtener más información sobre los efectos de DSP y el filtrado por voz.

-   Submezclación

    La submezcla combina varios sonidos en una sola secuencia de audio, por ejemplo, un sonido del motor compuesto, que se reproduce simultáneamente. Además, puede usar la submezcla para procesar y combinar partes similares de un juego. Por ejemplo, puede combinar todos los efectos de sonido del juego para permitir que se aplique una configuración de volumen de usuario mientras una configuración independiente controla el volumen de música. Combinado con DSP, la submezcla proporciona el tipo de enrutamiento y procesamiento de datos necesarios para los juegos de hoy en día. XAudio2 permite niveles arbitrarios de submezclación, lo que permite la creación de sonidos complejos y mezclas de juegos.

    Consulte [XAudio2 Audio Graph](xaudio2-audio-graph.md) y [XAudio2 Voices](xaudio2-voices.md) para obtener más información sobre la submezcla.

-   Compatibilidad con audio comprimido

    Una de las principales solicitudes de características de DirectSound ha sido la compatibilidad con audio comprimido. XAudio2 admite formatos comprimidos (ADPCM) de forma nativa con descompresión en tiempo de ejecución.

-   Compatibilidad mejorada con sonido multicanal y envolvente

    Se expande la compatibilidad con sonido multicanal, 3D y envolvente. El sonido 3D y envolvente ahora son mucho más flexibles y transparentes. XAudio2 quita el límite de 6 canales en sonidos multicanal y admite audio multicanal en cualquier tarjeta de audio compatible con varios canales. No es necesario que la tarjeta esté acelerada por hardware.

-   Procesamiento multirrate

    Para ayudar a minimizar el uso de CPU, XAudio2 proporciona la tecnología para crear varios gráficos de procesamiento de audio de baja velocidad. Esto puede reducir significativamente el uso de CPU al permitir que un juego procese audio a la velocidad del material de origen si la velocidad es inferior a 48 kHz.

-   Modelo de API de no bloqueo

    Con algunas excepciones, una llamada al método XAudio2 no bloqueará el motor de procesamiento de audio. Esto significa que un cliente puede realizar de forma segura un conjunto de llamadas de método en cualquier momento sin bloquear las llamadas de ejecución larga que provocan retrasos. Las excepciones son el método [**IXAudio2Voice::D estroyVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (que puede bloquear el motor hasta que la voz que se destruye finaliza el procesamiento) y los métodos que finalizan el subproceso de audio: [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) e [**IXAudio2::Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Tenga en cuenta que aunque las llamadas al método XAudio2 no bloquearán el motor de procesamiento de audio, los métodos XAudio2 contienen secciones críticas y pueden bloquearse en algunas circunstancias.

## <a name="when-to-use-xaudio2"></a>Cuándo usar XAudio2

XAudio2 está pensado principalmente para desarrollar motores de audio de alto rendimiento para juegos. Para los desarrolladores de juegos que quieren agregar efectos de sonido y música de fondo a sus juegos modernos, XAudio2 ofrece un motor de mezcla de gráfico de audio con baja latencia y compatibilidad con búferes dinámicos, reproducción sincrónica fiel a la muestra y conversión implícita de velocidad de origen. En comparación con WASAPI, XAudio2 solo requiere una cantidad mínima de código incluso para soluciones de audio complejas. En comparación con Media Foundation, XAudio2 es una API de C++ de bajo nivel y baja latencia diseñada para su uso en juegos.

En el caso de las aplicaciones que simplemente necesitan reproducción de música normal, el motor de Media Foundation puede ser una mejor coincidencia con los requisitos de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
