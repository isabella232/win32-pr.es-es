---
description: El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 Audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b461b89095152f3f8073a09a230e18f5e30fd7f42ffb60b4c45a32702094f70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707025"
---
# <a name="xaudio2-audio-graph"></a>XAudio2 Audio Graph

El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio. El gráfico toma un conjunto de secuencias de audio del cliente como entrada, las procesa y entrega el resultado final a un dispositivo de audio. Todo el procesamiento de audio tiene lugar en un subproceso independiente con una periodicidad definida por el cuántico del gráfico (actualmente 10 milisegundos en Microsoft Windows y 5 1/3 milisegundos en Xbox 360). Cada milisegundo cuántico, el subproceso se reactiva y dispersa los milisegundos cuánticos de datos de audio a través de todo el gráfico. Para obtener un ejemplo de creación de un gráfico de audio básico, vea Cómo: Compilar un procesamiento de [audio básico Graph](how-to--build-a-basic-audio-processing-graph.md).

Un gráfico de audio simple:

![un gráfico de audio simple](images/xaudio2-audio-graph.png)

El cliente puede controlar el estado del gráfico dinámicamente mientras se ejecuta. Las acciones de control pueden incluir agregar y quitar entradas y salidas, cambiar los efectos internos y las interconexiones, establecer parámetros en los efectos, habilitar y deshabilitar partes del gráfico, y así sucesivamente. Para obtener un ejemplo de cómo cambiar dinámicamente un gráfico de audio, vea Cómo: Agregar o quitar voces [dinámicamente de](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)un gráfico de audio Graph .

## <a name="processing-the-graph"></a>Procesamiento de la Graph

Cualquier llamada de método que afecte a cualquier objeto del gráfico se considera que está afectando a un cambio de estado del grafo. Graph cambios de estado incluyen los siguientes:

-   Creación y destrucción de voces
-   Inicio o detención de voces
-   Cambio de los destinos de una voz
-   Modificación de cadenas de efecto
-   Habilitación o deshabilitación de efectos
-   Establecimiento de parámetros en los efectos o en los SFC, filtros, volúmenes y mezcladores integrados

Cualquier conjunto de cambios de estado del grafo se puede combinar y realizar como una transacción atómica. Estas operaciones atómicas se conocen como conjuntos de operaciones. Se analizan en la introducción a los conjuntos de [operaciones de XAudio2.](xaudio2-operation-sets.md)

## <a name="internal-data-representation"></a>Representación de datos interna

Los datos de audio del gráfico XAudio2 siempre se almacenan y procesan en formato PCM de punto flotante de 32 bits. Sin embargo, el recuento de canales y la frecuencia de muestreo pueden variar dentro del gráfico. El formato en el que una voz determinada procesa el audio viene determinado por el tipo de voz y los parámetros utilizados para crear la voz.



| Tipo de voz                                                                                                      | Parámetros                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | El recuento de canales y la frecuencia de muestreo de las voces a las que la voz de origen envía audio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Argumentos *InputChannels* *y InputSampleRate* usados para crear la voz de submezcla/mastering. |



 

## <a name="format-conversion"></a>Conversión de formato

XAudio2 controla cualquier frecuencia de muestreo o conversiones de canal necesarias a medida que el audio viaja de una voz a otra, con las siguientes limitaciones:

-   Todas las voces de destino de una voz determinada deben ejecutarse con la misma frecuencia de muestreo
-   Los efectos de una cadena de efectos pueden cambiar el recuento de canales del audio, pero no su frecuencia de muestreo
-   El recuento de canales de salida de una cadena de efectos debe coincidir con el de las voces a las que envía.
-   No se puede realizar ningún cambio dinámico en el grafo, lo que interrumpiría las reglas anteriores

En el lado de entrada, las voces de origen pueden leer datos en cualquier formato PCM válido o en cualquiera de los formatos comprimidos compatibles con XAudio2. Si los datos de entrada se comprimen, se descodifican en PCM de punto flotante antes de realizar cualquier procesamiento adicional.

En el lado de la salida, las voces maestras solo pueden generar datos PCM. Estos datos siempre cumplirán las mismas restricciones descritas anteriormente para los datos PCM de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de audio](audio-graphs.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: agregar o quitar voces de un gráfico de audio dinámicamente](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[Cómo: usar voces de submezcla](how-to--use-submix-voices.md)
</dt> <dt>

[Cómo: crear un efecto en cadena](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



